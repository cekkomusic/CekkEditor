# Synth Editors — contesto per Claude

## Obiettivo
Editor/librarian MIDI nel browser (Web MIDI API, con SysEx) per i sintetizzatori di Francesco:
- **Sequential Take 5** — prima versione fatta: `take5/index.html`
- **Korg microKORG XL** — da fare
- **Moog Little Phatty** — da fare

Ogni editor deve:
- vedere lo strumento via USB MIDI e modificarne i parametri in tempo reale;
- aggiornare il pannello quando si muovono i controlli sullo strumento;
- leggere, salvare e richiamare suoni singoli e banchi (file .syx su disco + libreria nel browser);
- avere una grafica che richiama il pannello dello strumento, **senza loghi o marchi**;
- funzionare su PC (Chrome/Edge) e su Android (Chrome, synth collegato con cavo OTG).

## Scelte tecniche
- Un file HTML autosufficiente per strumento (HTML + CSS + JS inline, niente build).
- `navigator.requestMIDIAccess({sysex:true})`, con ripiego senza SysEx (solo parametri).
- Pubblicazione su **GitHub Pages**: serve HTTPS per la Web MIDI e rende facile l'uso da Android.
- Interfaccia in italiano. Layout a schede sotto gli 820 px.
- Conferma dentro la pagina prima di qualunque scrittura nella memoria dello strumento.

## Take 5 — dati chiave (da "Take 5 MIDI Implementation 1.2" e User's Guide 2.x)
- Manuali: https://sequential.com/wp-content/uploads/2021/09/Take-5-MIDI-Implementation-1.2.pdf
  e https://sequential.com/wp-content/uploads/2026/01/Take-5-Users-Guide-v2_3.pdf
- Parametri via NRPN: CC 99/98 numero, CC 6/38 valore (14 bit).
- SysEx: header `F0 01 35`.
  - Richiesta edit buffer: `F0 01 35 06 F7` → risposta `03` + dati compressi.
  - Richiesta programma: `F0 01 35 05 <banco 0-15> <prog 0-15> F7` → risposta `02 <banco> <prog>` + dati.
  - Device Inquiry: `F0 7E 7F 06 01 F7`, risposta con `01 35`.
- Dati in formato "packed MS bit": pacchetti da 8 byte, il primo contiene i bit alti dei 7 successivi (4096 byte → ~4695 byte MIDI).
- Banchi: 0-7 = User U1-U8, 8-15 = Factory F1-F8 (non sovrascrivibili).

## Punti aperti sul Take 5
- **Mappatura byte del dump → parametri non documentata.** L'editor ipotizza "indice byte = numero NRPN" (cutoff = byte 29 LSB + 30 MSB) e la scarta se più di 4 valori escono di scala. Va verificata con il Laboratorio (istantanea A/B + confronta).
- Posizione del nome del programma nel dump: per ora stimata cercando la prima stringa ASCII.
- Il documento MIDI è più vecchio del firmware: tipi FX (12 nel manuale, NRPN 0-8), modi arpeggio (5 vs 0-2), destinazioni modulazione oltre 54, NRPN 67 e 74 (ipotesi: destinazioni LFO).
- Formato dei valori bipolari (centro 127?) e del Noise (centro 64?) da confermare.

## microKORG XL — dati chiave (da Owner's Manual, `docs/Microkorg xl manual.pdf`, pp. 28-29, 59-62, 80-93)
- Il manuale d'uso NON contiene il formato dei dati SysEx: rimanda alla «MIDI Implementation» separata sul sito Korg. Da procurare.
- SysEx: header `F0 42 3n 7E` (n = canale globale 0-F), poi function ID. Supportati anche Master Volume `F0 7F nn 04 01 vv mm F7` e Master Fine Tune `F0 7F nn 04 03 vv mm F7`.
- Dimensioni dump: 1 programma 402 byte, tutti i programmi 51.712 byte, global 121 byte. Ricezione dump solo con GLOBAL «PROTECT» = OFF e MIDI FLT «SYS EX» = ENABLE.
- Programmi: 128 (A11-B88), Bank Select CC0=0 CC32=0 + Program Change 0-127. CC0=32/CC32=32|33 + PC = carica un timbro di un altro programma nel Timbre 1|2.
- Parametri del pannello via **CC a 7 bit** (mappa riassegnabile in CC MAP; valori iniziali p. 90-92), per es.:
  OSC1 Wave CC8, Osc Mod CC9, C1 CC15, C2 CC17; OSC2 Wave CC18, Mod CC19, Semitone CC20, Tune CC21;
  Mixer CC23/24/25; Filtro1 Cutoff CC74, Reso CC71, Type Bal CC27, Routing CC26, EG1 Int CC79, Key Trk CC28;
  Filtro2 Cutoff CC30, Reso CC68, Type CC29, EG1 Int CC69, Key Trk CC82; Amp Level CC7, Pan CC10; WS Depth CC83;
  EG1 ADSR CC85-88; EG2 ADSR CC73/75/70/72; LFO1 Wave CC89 Freq CC90; LFO2 Wave CC102 Freq CC76;
  Patch1-6 Intensity CC103-108; EQ Lo CC110 Hi CC109; FX1 Dry/Wet CC115 Ctrl CC12/112; FX2 Dry/Wet CC116 Ctrl CC13/113;
  Unison CC3, Portamento CC5. Valori a fasce (es. Wave 0-15 SAW, 16-31 PULSE...): inviare il centro della fascia.
- **NRPN solo con Data Entry MSB (CC6)**, niente CC38. Arp: 00/02 On, 00/04 Latch, 00/07 Type, 00/0A Gate, 00/0B Select timbro.
  Virtual Patch: 04/00-05 Source 1-6, 04/08-0D Dest 1-6. Vocoder: 04/40-4F livelli bande, 04/50-5F pan bande; 05/04 Vocoder Sw; 05/00 Voice Mode.
- Due timbri: in MULTI il Timbre 2 usa il canale «T2MIDI.CH»; il resto viaggia sul canale globale.
- Porte USB: «KBD/KNOB» (uscita dal synth) e «SOUND» (ingresso al generatore). MIDI «ROUTING» deve includere USB.

## Come si lavora
Claude non può collegarsi agli strumenti: Francesco prova, riporta il log del Laboratorio o il comportamento, e si corregge a iterazioni. Mantenere compatibilità con i file .syx e con i backup .json già esportati.
