# Geocodifica in Python
## Che cos'è la geocodifica?
La geocodifica è il processo di conversione degli indirizzi in coordinate geografiche. Questo significa trasformare gli indirizzi in coppie (latitudine;longitudine). Le coordinate ottenute possono essere utilizzate per posizionare degli indicatori su una mappa.
La geocodifica rappresenta una parte essenziale di molti processi geospaziali, per esempio permette di visualizzare dei punti di vendita su una mappa,  calcolare un percorso ottimizzato per una consegna o cercare nel raggio di un punto di origine.

## Geocodifica in Python
In Python sono disponibili molte librerie per tale scopo.La più veloce è l' API di Google Maps, ideale nel caso di un gran numero di indirizzi da convertire in coordinate in modo rapido.
Da qualche anno l'API di Google Maps non è più gratuita, pertanto in questo articolo utilizzerò la sua “naturale” alternativa ossia l'API OpenStreetMap, completamente gratuita. Tuttavia, l'API OpenStreetMap presenta l’inconveniente di essere molto più lenta e anche leggermente meno precisa.
Altra possibilità sarebbe l’utilizzo, per esempio, di MapQuest, che però richiede una semplice registrazione per ottenere una Consumer Key gratuita fino a 15000 richieste al mese.

## API OpenStreetMap
Passiamo alla parte pratica!
Utilizzerò questa API per ottenere le coordinate geografiche delle Istituzioni scolastiche presenti in Puglia. Per ridurre i tempi di elaborazione dell’API OpenStreetMap, limiterò la ricerca alle sole istituzioni scolastiche presenti in provincia di Lecce.
Per ricavare l'elenco delle Istituzioni Scolastiche Pugliesi, utilizzo gli Open Data dell'USR Puglia disponibili al seguente indirizzo https://www.pugliausr.gov.it/index.php/70-la-scuola-in-numeri
