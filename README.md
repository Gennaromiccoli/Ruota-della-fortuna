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

## Su Fire TV / Android TV
- Usa un browser vero: **Silk** su Fire TV, oppure **Fully Kiosk Browser** (Fire TV e Android TV) con l'opzione "Keep Screen On" e l'indirizzo del tabellone come pagina iniziale.
- Il tabellone chiede allo schermo di restare acceso (Wake Lock + video muto invisibile), ma alcune app con browser integrato (es. Downloader) ignorano la richiesta.
- In più, sulla Fire TV imposta lo screensaver su "Mai".

## Regole predefinite (modificabili in "Nuova partita")
- **PASSA** (lo 0 della ruota): il turno passa al concorrente successivo.
- **BANCAROTTA**: si perdono i soldi della manche **e** quelli conservati nelle manche precedenti.
- **BONUS**: si chiama una consonante, poi si gira: la consonante vale il valore uscito e se ne chiama subito un'altra allo stesso valore. In quel giro gli spicchi senza valore non contano: si rigira.
- Chi risolve incassa i soldi della manche + **1000 €**; gli altri perdono i soldi della manche.
- Lettera già chiamata, consonante/vocale assente o soluzione sbagliata → turno al successivo.
- A fine partita vince chi ha il totale più alto; in caso di parità si può giocare una manche di spareggio.

## Manche speciali (ispirate alla trasmissione attuale)
Ogni manche si configura a parte; il pulsante **📺 Scaletta stile TV** prepara 6 manche già pronte.
- **Manche lampo**: niente ruota, le lettere si accendono da sole; chi si prenota (tocca il suo nome) e indovina vince un premio fisso. Chi sbaglia resta fuori da quella frase.
- **🃏 Jolly**: spicchio digitale; chi lo prende e chiama una consonante giusta conserva il Jolly e lo può usare una volta contro BANCAROTTA, PASSA o un errore.
- **❓ Mistero**: dopo una consonante giusta si sceglie se scoprirlo: premio alto (10.000 € di default) oppure bancarotta.
- **⚡ Express**: dopo una consonante giusta si può salire sull'Express: consonanti a valore fisso e vocali senza girare, finché si risolve; un errore fa perdere i soldi della manche.
- Per ogni manche anche valori ×2/×3 e tempo massimo per turno.
- Jolly, Mistero ed Express compaiono sulla ruota digitale; con la ruota manuale hanno i loro pulsanti.

## Gioco finale delle 3 buste
Il vincitore affronta tre frasi con un tema comune e un solo cronometro (60 secondi di default):
1. **Busta 1**: lettere regalate (R S T L N E) + 3 consonanti e 1 vocale scelte dal concorrente.
2. **Busta 2**: si vedono la prima e l'ultima lettera di ogni parola.
3. **Busta 3**: le lettere compaiono da sole una alla volta.

"Stop" passa alla busta successiva. Ogni frase risolta apre una busta verde con un premio nascosto (estratto tra quelli indicati, fino a 200.000 €); le altre diventano rosse e mostrano il premio perso.

**↶ Annulla** (o Ctrl+Z) torna indietro di un'azione in caso di errore. La partita viene salvata nel browser e si riprende ricaricando la pagina.
