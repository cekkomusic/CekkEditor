# Synth Editors — contesto per Claude

## Obiettivo
Editor/librarian MIDI nel browser (Web MIDI API, con SysEx) per i sintetizzatori di Francesco:
- **Sequential Take 5** — prima versione fatta: `take5/index.html`
- **Korg microKORG XL** — prima versione fatta: `mkxl/index.html`
- **Moog Little Phatty** — prima versione fatta: `phatty/index.html`

Ogni editor deve:
- vedere lo strumento via USB MIDI e modificarne i parametri in tempo reale;
- aggiornare il pannello quando si muovono i controlli sullo strumento;
- leggere, salvare e richiamare suoni singoli e banchi (file .syx su disco + libreria nel browser);
- avere una grafica che richiama il pannello dello strumento, **senza loghi o marchi**;
- funzionare su PC (Chrome/Edge) e su Android (Chrome, synth collegato con cavo OTG).

## Scelte tecniche
- **App unica «CekkEditor»** (`index.html` nella radice), installabile sul telefono come PWA (`manifest.webmanifest`, `sw.js`, `icons/`).
  All'apertura: impostazioni MIDI (porte e canale per ogni synth, trovate da sole per nome) e carosello orizzontale dei synth.
  L'editor scelto si apre a tutto schermo in un iframe.
- La app espone `window.CekkMIDI` (`access`, `sysex`, `ports(id)`, `on(fn)`): l'editor nell'iframe usa quelle porte invece di chiedere il MIDI da sé.
  Ogni editor resta un file HTML autosufficiente (HTML + CSS + JS inline, niente build) che funziona anche aperto da solo (`take5/`).
  Per aggiungere un synth: voce in `SYNTHS` dentro `index.html` (`ready:true`, `url`), cartella con il suo `index.html`, URL in `CORE` di `sw.js`.
- In ascolto con `addEventListener("midimessage")` + `open()`, non `onmidimessage`, perché le porte sono condivise.
- `navigator.requestMIDIAccess({sysex:true})`, con ripiego senza SysEx (solo parametri).
- Pubblicazione su **GitHub Pages** dal ramo `ccr-650e1c9a-a8zli2`, cartella radice: https://cekkomusic.github.io/CekkEditor/
- Service worker «prima la rete»: gli aggiornamenti arrivano subito; la cache serve solo senza connessione. Cambiare `CACHE` in `sw.js` se cambia l'elenco `CORE`.
- Interfaccia in italiano. Layout a schede sotto gli 820 px.
- Grafica: ogni editor richiama il proprio synth (colori, manopole, disposizione), **senza loghi o marchi**. Le schede del carosello sono disegnate in `ART` dentro `index.html`.
  Le foto inviate da Francesco (prodotto e editor di terze parti) servono solo da riferimento e non vanno messe nel repository.
  - **Take 5** (fatto): corpo nero, pannello #222326, fila alta a sezioni separate da filetti con titolo sopra; fascia centrale ardesia #3a3f4a
    (Oscillators, Mixer, Filter, Envelopes) con titoli grandi in basso; manopole nere a calotta grigio chiaro con indice nero e tacche bianche;
    Cutoff grande con tacche arancioni #ff6a1f; tasti quadrati neri che si accendono di rosso; display OLED bianco-azzurro; display programma rosso a 7 segmenti.
  - **microKORG XL** (fatto): corpo nero, fascia frontale in alluminio spazzolato, due manopole grandi nere (Genre / Category), display ambra #f7a531,
    piccole manopole a destra, 37 mini tasti, presa microfono al centro. Gli editor di riferimento mostrano: pagina Program con lista dei 128 programmi
    (A11-B88) su più colonne in carattere da display; pagina Timbre con forme d'onda e curve EG/filtro disegnate su sfondo nero; Virtual Patch a 6 righe.
  - **Little Phatty** (fatto): pannello nero con fiancate grigie, intestazioni di sezione su fascia sottile (Modulation, Oscillators, Filter,
    Envelope Generators, Output), quattro manopole grandi con anello di LED arancioni, tasti arrotondati grigio-blu #4c5763 che si accendono
    arancio o rosso, display LCD grigio chiaro, ruote illuminate arancio. Gli editor di riferimento hanno grafici degli inviluppi Amp/Filter e selettori a lista verticale (Source, Destination, Octave, Filter Poles).
- Conferma dentro la pagina prima di qualunque scrittura nella memoria dello strumento.
- Librerie di Take 5 e microKORG XL: caselle di selezione (`S.sel`, non salvata). Export e scrittura multipla usano i suoni spuntati nell'ordine della lista:
  Take 5 fino a 16 nelle posizioni 1… del banco scelto; microKORG XL in programmi consecutivi da «Dal programma».

## Take 5 — dati chiave (da "Take 5 MIDI Implementation 1.2" e User's Guide 2.x)
- MIDI Implementation 1.2 nel repository: `docs/Take-5-MIDI-Implementation-1.2.pdf` (letta). Manuali: https://sequential.com/wp-content/uploads/2021/09/Take-5-MIDI-Implementation-1.2.pdf
  e https://sequential.com/wp-content/uploads/2026/01/Take-5-Users-Guide-v2_3.pdf
- Parametri via NRPN: CC 99/98 numero, CC 6/38 valore (14 bit).
- SysEx: header `F0 01 35`.
  - Richiesta edit buffer: `F0 01 35 06 F7` → risposta `03` + dati compressi.
  - Richiesta programma: `F0 01 35 05 <banco 0-15> <prog 0-15> F7` → risposta `02 <banco> <prog>` + dati.
  - Device Inquiry: `F0 7E 7F 06 01 F7`, risposta con `01 35`.
- Dati in formato "packed MS bit": pacchetti da 8 byte, il primo contiene i bit alti dei 7 successivi (4096 byte → ~4695 byte MIDI).
- Banchi: 0-7 = User U1-U8, 8-15 = Factory F1-F8 (non sovrascrivibili).
- Dal documento: NRPN 0-66, 68-73, 75-124, 163-171 (programma), **4198 SeqOnOff e 4199 SeqRecordArm** (unici comandi del sequencer: le note degli step
  non sono esposte via MIDI), globali 4096-4122. NRPN 67 e 74 non compaiono. FXSelect 0-8 nel documento. Esiste anche la mappa CC (Param Snd/Rcv = CC)
  con valori a 7 bit; l'editor usa gli NRPN. Richiesta globali `F0 01 35 0E F7` (dump solo in uscita, i globali si cambiano via NRPN).

## Punti aperti sul Take 5
- **Mappatura byte del dump → parametri non documentata.** Prima prova reale (21/10): il banco si legge ma si vede solo il nome, l'ipotesi
  "indice byte = numero NRPN" è sbagliata. Aggiunto nel Laboratorio «Impara la mappa del dump» (`learnMap`): per ogni parametro invia via NRPN due valori di prova,
  rilegge l'edit buffer e cerca il byte (o la coppia LE/BE, o un byte con scarto costante) che li contiene; alla fine ripristina il suono di partenza.
  La mappa sta in localStorage `take5-dumpmap-v1` e si copia con «Copia mappa» (testo «MAPPA TAKE 5 {...}»): quando Francesco la incolla in chat,
  va resa predefinita nell'editor.
- Posizione del nome del programma nel dump: per ora stimata cercando la prima stringa ASCII.
- Chiarito con la User's Guide 2.3 (`docs/Take-5-Users-Guide-v2_3.pdf`): 12 tipi di effetto (Stereo Delay…Lo-Fi, ordine e nomi delle 3 manopole come nell'editor),
  5 modi arpeggio (Up, Down, Up+Down, Random, Assign), 20 sorgenti e 58 destinazioni di modulazione (0-57, appendici A/B), forme LFO Tri/Saw/RevSaw/Square/S&H,
  Noise bipolare (sinistra rosa, destra bianco). Le destinazioni LFO esistono (p. 32): NRPN 67 e 74 restano dedotti, da verificare.
- Sequencer (guida p. 47): 64 step, accordi fino a 5 note, velocity, legature e pause, salvato col programma. Via MIDI solo Play/Record (NRPN 4198/4199).
- Formato dei valori bipolari (centro 127?) e del Noise (centro 64?) da confermare.

## microKORG XL — dati chiave (da Owner's Manual, `docs/Microkorg xl manual.pdf`, pp. 28-29, 59-62, 80-93)
- **Formato SysEx completo in `docs/microKORG_XL_MIDIimp.txt`** (MIDI Implementation rev. 1.01, 2009): mappa byte per byte del programma (TABLE 1-6) e dei globali (TABLE 7).
  - Header `F0 42 3g 7E` (g = canale globale). Richieste: `10` edit buffer, `1C pp 00` programma pp (0-127), `0E` globali, `11 pp 00` scrivi l'edit buffer nel programma pp.
  - Risposte/dump: `40` edit buffer, `4C pp 00` programma, `51` globali. Esiti: `23` caricato, `24` errore (es. protect), `26` formato errato, `21`/`22` scrittura ok/errore.
  - Parameter Change `41 pp PP qq QQ vv VV` (ID, Sub ID, valore 14 bit con segno; ID:SubID nelle tabelle). Il synth lo invia quando si muovono manopole/tasti → serve per aggiornare il pannello.
  - Device Inquiry: risposta `F0 7E 0g 06 02 42 7E 00 00 00 …`. Esiste anche Search Device `F0 42 50 00 dd F7`.
  - Dati compressi 7→8 come il Take 5 (primo byte = bit 7 dei 7 successivi, bit0 = primo byte).
  - Programma: 0-7 nome ASCII, 16-111 Timbre 1, 112-207 Timbre 2, 208-285 Vocoder, 286-333 FX, 334-335 tempo, 336 Arp on/key sync, 338-345 Arp.
  - Da verificare: la NOTE 1 dice 342 byte (391 compressi) ma la TABLE 1 arriva al byte 345; il manuale d'uso dice 402 byte per «1 Prog». Controllare con un dump reale.
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

## Punti aperti sul microKORG XL (editor `mkxl/index.html`)
- Il pannello legge e scrive un buffer di programma con la mappa esatta delle TABLE 1-6 (`ofs`, bit `sh`/`w`, `id`/`sub`); le modifiche partono come Parameter Change.
- Ordine dei byte di ID/Sub ID nel Parameter Change: la tabella (8) dice LSB prima, la NOTE 4 dice MSB prima. Predefinito LSB; l'editor passa da solo all'altro ordine
  se il synth manda un ID riconoscibile solo così (e lo salva). Commutabile a mano nel Laboratorio.
- Valori bipolari: la NOTE 4 dice «signed value», quindi si inviano come valore − centro (es. Transpose +5 → 5). Commutabile nel Laboratorio.
- Lunghezza del programma 342 o 346 byte: si usa quella del dump ricevuto; il Laboratorio avvisa se è diversa.
- «Scrivi nel synth»: invia l'edit buffer (40) e poi Program Write Request (11 pp 00). La libreria scrive con Program Data Dump (4C pp 00).
- Parametri non ancora nel pannello: Formant Hold, globali (TABLE 7), CC MAP.

## Little Phatty — dati chiave (da `docs/Little_Phatty_StageII_Manual.pdf`, Stage II, MIDI Chart v2.2 del 2009)
- Stage II: MIDI su DIN e **USB**. In MASTER → MIDI SETUP: ingresso e uscita DIN/USB (predefinito DIN/USB), canali In/Out separati (predefinito 1), Local Control, MIDI Merge.
- **Parametri solo via CC a 7 bit** (nessun NRPN, nessun Parameter Change SysEx). Cutoff e Mod Wheel a 14 bit: Cutoff CC19 MSB + CC51 LSB, Mod Wheel CC1 + CC33.
  Il synth trasmette i CC quando si muovono le manopole e quando si cambiano i parametri nei menu → il pannello si aggiorna da solo.
- Tabella CC (p. 55-56): Glide on/off CC65 (0/64); LFO Rate CC3; Mod Amount CC6; Mod Source CC68 (0 Tri,16 Sq,32 Saw,48 Ramp,64 Filt Env,80 Osc2);
  Mod Dest CC69 (0 Pitch,16 Filt,32 Wave,48 Osc2); LFO Sync CC102 (0 Int,64 MIDI); LFO Clock Div CC103; Mod Src 5 CC104 (0 Filt,64 S&H);
  Mod Src 6 CC105 (0 Osc2,64 Noise); Mod Dest 2 CC106 (0 Off,25 Pitch,50 Filt,75 Wave,100 Osc2);
  Osc1 Octave CC74 (0 16',32 8',48 4',64 2'); Osc1 Wave CC9; Osc1 Level CC15; Glide Rate CC5; Sync CC77 (0/64); Osc2 Octave CC75; Osc2 Freq CC10;
  Osc2 Wave CC11; Osc2 Level CC16; Bend Up CC107; Bend Down CC108; Cutoff CC19/51; Resonance CC21; KB Amount CC22; EG Amount CC27; Overload CC18;
  Filter Poles CC109 (0,32,64,96 = 1-4); Filter Vel Sens CC110 (-8…+8 = 0,12,19,…,117 a passi di 7);
  Filter EG ADSR CC23-26; Volume EG ADSR CC28-31; EGR Release CC111 (0/64); EGR Legato CC112 (0 On,43 Off,86 Reset);
  Arp Enable CC113; Arp Run/Stop CC90; Arp Clock coarse CC4 (BPM/3) + fine CC36 ((BPM-coarse*3)*10); Arp Clock Source CC114 (0 Int,43 LFO,86 MIDI);
  Arp Clock Div CC115; Arp Range CC116 (0,19,38,57,71,90,109 = -3…+3); Arp Pattern CC117 (0 Up,43 Down,86 Order); Arp Mode CC118 (0 Loop,43 Back/Forth,86 Once);
  Arp Latch Enable CC119; Arp Latch CC91; Volume CC7; Key Priority CC88 (0 Glob,32 Low,64 High,96 Last).
  Clock Divider (CC103/115): 0 1/32, 8 1/32., 16 1/16, 24 1/16., 32 1/8, 40 1/8., 48 1/4, 56 1/4., 64 1/2, 72 1/2., 80 WH, 88 WH+1/4, 96 WH+1/2, 104 WH+1/2., 112 WH+WH.
- Con il Pot Mapping attivo in una sezione, quella manopola manda il CC scelto dall'utente invece di quelli in tabella (p. 37).
- Program Change 0-99 (100 preset).
- SysEx: il manuale **non documenta il formato** né un messaggio di richiesta. I dump partono dal synth (MASTER → SYSEX: Send Current Preset,
  Send All Presets, Bulk Dump) e il synth li riceve sempre: un preset singolo viene **scritto subito nella posizione corrente** (attenzione: sovrascrive),
  un banco sostituisce tutti i preset. L'editor quindi: riceve e salva i .syx inviati dal synth, li rimanda con conferma, e legge i valori del pannello dai CC.
  La mappatura byte→parametro del dump va ricavata col Laboratorio, se serve.

## Punti aperti sul Little Phatty (editor `phatty/index.html`)
- Il synth non dice i valori del preset: il pannello mostra «—» finché un parametro non viene mosso (dall'editor o dal synth). `S.known` tiene traccia di quelli noti.
- Libreria a due parti: «Pannelli» (valori CC noti, rimandati come CC senza toccare la memoria) e «Dump SysEx» ricevuti dal synth
  (messaggi che arrivano entro 1,5 s uno dall'altro = un dump), rimandati tali e quali con conferma.
- Da verificare: lunghezza e struttura dei dump (preset singolo vs banco), scala reale di Bend Up/Down (0-127 nella tabella), nome della porta USB.

## Ricette (suoni preparati in chat) — impostate, da usare dopo la prova degli editor
- Formato e istruzioni in `ricette/README.md`, chiavi di ogni synth in `ricette/CHIAVI.md` (generato dagli editor: rigenerarlo se cambiano i parametri).
- Un file JSON per suono `{synth, nome, descrizione, parametri:{chiave:valore}}` + voce in `ricette/index.json`. Chiavi: Take 5 = numero NRPN,
  microKORG XL = nome del parametro (`t0.f1cut`…; FX: prima `fxNtype`, poi `fxNpK` secondo la EFFECT PARAMETER STRUCTURE), Little Phatty = `cc`+numero.
- Ogni editor: lista «Ricette» → «Prova» applica e invia come modifiche di parametro (mai scrittura in memoria); «Importa ricetta», «Esporta pannello come ricetta».
- Francesco ha chiesto di NON preparare suoni finché gli editor non funzionano bene sugli strumenti reali. Le `*-prova.json` servono solo a verificare il meccanismo.

## Come si lavora
Claude non può collegarsi agli strumenti: Francesco prova, riporta il log del Laboratorio o il comportamento, e si corregge a iterazioni. Mantenere compatibilità con i file .syx e con i backup .json già esportati.
