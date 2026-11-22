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

## Telecomando dal telefono
La TV (o il PC collegato alla TV) mostra tabellone, ruota e punteggi; il telefono fa da conduttore.
1. Apri il tabellone sulla TV e premi **📱 Telecomando** (in alto, o "Collega il telefono" in Nuova partita).
2. Inquadra il QR code con il telefono (oppure apri il sito sul telefono e inserisci il codice di 5 caratteri).
3. Dal telefono crei la partita, scrivi la frase (non compare mai sulla TV), giri la ruota o scegli lo spicchio, chiami le lettere, confermi le soluzioni e annulli gli errori. Sul telefono la soluzione è sempre visibile.

Il collegamento è diretto tra TV e telefono (WebRTC con PeerJS); il servizio pubblico gratuito di PeerJS serve solo a farli trovare. Serve internet su entrambi, meglio sullo stesso Wi-Fi. Se il telefono va in standby si ricollega da solo. Funziona dal sito GitHub Pages, non dall'anteprima su claude.ai.

## Regole predefinite (modificabili in "Regole avanzate")
- **PASSA** (lo 0 della ruota): il turno passa al concorrente successivo.
- **BANCAROTTA**: si perdono i soldi della manche **e** quelli conservati nelle manche precedenti.
- **BONUS**: il concorrente chiama una consonante e poi gira la ruota: la consonante vale il valore uscito e se ne chiama subito un'altra allo stesso valore. In quel giro BANCAROTTA, PASSA e BONUS non contano: si rigira. La seconda consonante segue le regole normali (se non c'è, il turno passa).
- Chi risolve incassa i soldi della manche + **1000 €**; gli altri perdono i soldi della manche.
- Lettera già chiamata, consonante/vocale assente o soluzione sbagliata → turno al successivo.
- A fine partita vince chi ha il totale più alto; in caso di parità si può giocare una manche di spareggio.

## Manche speciali e gioco finale (in "Nuova partita")
- Per ogni manche: valori della ruota normali, doppi o tripli, e un eventuale tempo massimo per turno (allo scadere il turno passa).
- **Gioco finale** (opzionale): il vincitore riceve le lettere regalate (default R S T L N E), sceglie 3 consonanti e 1 vocale e ha pochi secondi per risolvere. Premio configurabile.

**↶ Annulla** (o Ctrl+Z) torna indietro di un'azione in caso di errore. La partita viene salvata nel browser e si riprende ricaricando la pagina.
