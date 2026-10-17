# Ricette

Una **ricetta** è un suono descritto come elenco di valori dei parametri. Si prepara in chat; l'editor del synth la applica al pannello e la invia al synth come normali modifiche di parametro (NRPN sul Take 5, Parameter Change sul microKORG XL, CC sul Little Phatty). La memoria del synth non cambia finché il suono non viene salvato.

## Formato

Un file JSON per suono, in questa cartella:

```json
{
  "synth": "take5",
  "nome": "Nome del suono",
  "descrizione": "Una riga su com'è fatto",
  "parametri": { "29": 600, "31": 40 }
}
```

- `synth`: `take5`, `mkxl` oppure `phatty`.
- `parametri`: chiave → valore, nelle unità dell'editor. L'elenco completo delle chiavi è in [`CHIAVI.md`](CHIAVI.md), generato dagli editor.
  I parametri che non compaiono restano come sono sul synth: conviene partire da un suono base noto.
- Sul microKORG XL `nome` diventa anche il nome del programma (8 caratteri).

Ogni editor ha anche «Esporta pannello come ricetta», che salva il suono attuale in questo formato: è il modo più sicuro per avere un esempio aggiornato.

## Elenco

Gli editor mostrano le ricette elencate in [`index.json`](index.json), filtrate per synth:

```json
[{ "synth": "take5", "file": "take5-prova.json", "nome": "…", "descrizione": "…" }]
```

Per aggiungere una ricetta: crea il file, aggiungi la voce in `index.json`.

## Stato

Le tre ricette `*-prova.json` servono solo a verificare il meccanismo (un suono semplice e innocuo), non sono suoni curati.
Prima di preparare ricette vere vanno provati gli editor sugli strumenti reali: le ricette usano le stesse scale di valori degli editor.
