# ⚽ Asta Live

Assistente per l'**asta del fantacalcio** in un singolo file HTML. Nessun server, nessuna
build, nessuna dipendenza: apri il file nel browser e sei operativo.

Nato per gestire in diretta l'asta di una lega classic, tenendo sotto controllo budget,
reparti e prezzi di mercato mentre i giocatori vengono battuti.

## Funzionalità

- **Modalità Classic / Mantra** — selettore in alto. **Classic**: 850 crediti, rose da 30, ruoli P/D/C/A. **Mantra**: 500 crediti, rose da 29 (4 portieri + 25 di movimento), ruoli Mantra (Pc, A, T, W, C, M, E, B, Dc, Dd, Ds, Por). Le due aste hanno **stato salvato separato**: puoi passare dall'una all'altra senza perdere nulla.
- **Gestione rosa e budget** — 850 crediti, rose da 30 (4 portieri, 9 difensori, 10 centrocampisti, 7 attaccanti)
- **Target per reparto** con riequilibrio automatico del budget residuo
- **XI suggerito** sui giocatori ancora disponibili, per modulo (3-4-3, 3-5-2, 4-3-3, 4-4-2, 4-5-1)
- **Tracking dei rivali** — chi ha comprato cosa, residuo e reparti scoperti di ogni squadra (solo in Classic; in Mantra è nascosto: gli altri si segnano solo con «altri» per toglierli dai disponibili, senza squadra né prezzo)
- **Statistiche di mercato live** — quanto si sta pagando rispetto al prezzo atteso, colpi più costosi
- **Profili multipli** per gestire più aste separate
- **Export CSV** e import da testo incollato
- **Assistente AI opzionale** (vedi sotto)

Tutto lo stato è salvato nel `localStorage` del browser.

## Uso

Scarica `asta-live.html` e aprilo nel browser. È tutto qui.

## Assistente AI (opzionale)

Il tool può interrogare un modello per consigli in tempo reale ("conviene Lautaro a 90?").
È **disattivato finché non lo configuri**: apri ⚙️ **Config** e inserisci

- **Endpoint** — un URL Azure OpenAI in formato Responses API:
  `https://TUA-RISORSA.openai.azure.com/openai/responses?api-version=2025-04-01-preview`
- **API key** — la tua chiave
- **Model / deployment** — es. `gpt-5-mini`

> 🔒 La API key resta **solo nel tuo browser**: non viene mai scritta nel file HTML né nei
> backup esportati. Se condividi il file dopo averla configurata, la chiave non parte con lui.

## Dati dei calciatori

Il file include una lista di giocatori con quotazioni, FVM, media voto e fantamedia.

> ⚠️ **I dati dei calciatori provengono dalla lista ufficiale di [Fantacalcio.it](https://www.fantacalcio.it)
> e restano di proprietà dei rispettivi titolari.** La licenza MIT di questo progetto copre
> esclusivamente il codice, non il dataset incorporato.

I dati sono una fotografia di inizio stagione 2026/27: MV e FM sono calcolate su pochissime
giornate e vanno lette con cautela.

## Licenza

[MIT](LICENSE) © 2026 Salvatore Postiglione — vedi la nota sui dati qui sopra.
