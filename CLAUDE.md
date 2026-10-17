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

## Come si lavora
Claude non può collegarsi agli strumenti: Francesco prova, riporta il log del Laboratorio o il comportamento, e si corregge a iterazioni. Mantenere compatibilità con i file .syx e con i backup .json già esportati.
