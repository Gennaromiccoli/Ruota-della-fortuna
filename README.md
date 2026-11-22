# Tabellone della Ruota

Tabellone digitale da affiancare alla ruota fisica (Clementoni) per giocare a casa.
È un unico file: apri `index.html` nel browser (meglio su un TV o un portatile a schermo intero).

## Come si gioca
1. **Nuova partita**: inserisci i concorrenti (quanti vuoi) e il numero di manche.
2. All'inizio di ogni manche il conduttore scrive **titolo** e **frase**. La frase resta nascosta (👁 per mostrarla).
3. Al turno si gira la ruota:
   - **Ruota digitale**: premi *Gira la ruota*.
   - **Ruota manuale**: gira quella vera e tocca lo spicchio uscito.
4. Con un valore in € si chiama una consonante: le caselle si accendono da sole e si incassa valore × lettere trovate.
5. **Compra vocale**: 200 €. **Risolvi**: il conduttore conferma se la soluzione è giusta o sbagliata.

## Regole predefinite (modificabili in "Regole avanzate")
- **PASSA** (lo 0 della ruota): il turno passa al concorrente successivo.
- **BANCAROTTA**: si perdono i soldi della manche **e** quelli conservati nelle manche precedenti.
- **BONUS**: il concorrente chiama una consonante, poi rigira la ruota e ne chiama un'altra. In quel giro BANCAROTTA e PASSA non contano: si rigira. La consonante bonus vale 0 € (configurabile).
- Chi risolve incassa i soldi della manche + **1000 €**; gli altri perdono i soldi della manche.
- Lettera già chiamata, consonante/vocale assente o soluzione sbagliata → turno al successivo.
- A fine partita vince chi ha il totale più alto; in caso di parità si può giocare una manche di spareggio.

## Manche speciali e gioco finale (in "Nuova partita")
- Per ogni manche: valori della ruota normali, doppi o tripli, e un eventuale tempo massimo per turno (allo scadere il turno passa).
- **Gioco finale** (opzionale): il vincitore riceve le lettere regalate (default R S T L N E), sceglie 3 consonanti e 1 vocale e ha pochi secondi per risolvere. Premio configurabile.

**↶ Annulla** (o Ctrl+Z) torna indietro di un'azione in caso di errore. La partita viene salvata nel browser e si riprende ricaricando la pagina.
