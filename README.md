# Creare una mappa con Folium library
L’importanza delle mappe è indiscussa; ormai rappresentano un aiuto nell’esplorazione del mondo, nel raggiungere un luogo di destinazione e/o interesse.
Questo articolo si ricollega con il lavoro svolto nel precedente articolo relativo all’introduzione alla geocodifica e integra i risultati ottenuti attraverso la visualizzazione dei dati su di una mappa per mezzo della libreria di Python Folium.

## Cos’è Folium?
Come detto Folium è una libreria di Python utilizzata per la visualizzazione di dati geospaziali, facile da usare e potente allo stesso tempo. Folium è un wrapper Python per Leaflet.js, libreria JavaScript open source fondamentale per la stampa di mappe interattive.
La prima operazione da svolgere è proprio l’installazione di Folium nel proprio ambiente di lavoro, usando il comando:

<b>pip install Folium</b>

## Creare e visualizzare mappe con Folium
Prendiamo in considerazione un esempio pratico: si voglia visualizzare su una mappa la posizione delle varie Istituzioni Scolastiche. Si parte dalla lettura dei dati ricavati e memorizzati in un file .csv. 
I dati così come caricati non sono immediatamente utilizzabili, per due ragioni: la prima perché, come visto, per alcuni Istituti non è stato possibile ricavare le coordinate e nella relativa cella è riportato semplicemente il valore “-1”; il secondo motivo è che le coordinate così come visualizzate non sono gestibili direttamente dalla libreria Folium, è necessario separare i valori di latitudine da quelli relativi alla longitudine.

## Operare sul DataFrame
Apporto le modifiche nel precedente programma in modo da eliminare i valori non necessari e aggiungere la colonna relativa alla “latitudine” e quella relativa alla “longitudine”.
Procedo al salvataggio del file in .csv.
A questo punto realizzo un nuovo programma, recupero il DataFrame.
La prima operazione da fare è costruire l’oggetto mappa che “centro” in un punto ideale di coordinate pari al valore medio e fisso lo zoom iniziale.

## Tracciare gli indicatori sulla Mappa
Lo scopo è quello di contrassegnare con degli indicatori la posizione degli Istituti Scolastici sulla mappa. Un pò come succede quando si utilizza Google Maps per la navigazione, la tua posizione è contrassegnata da un indicatore e la tua destinazione è contrassegnata da un altro indicatore. Gli indicatori sono tra le cose più importanti e utili su una mappa.
Per fare ciò si utilizza una classe folium.Marker() alla quale basta passare la latitudine e la longitudine della posizione, menzionare il popup e il suggerimento e aggiungerlo alla mappa. Questa operazione avviene in due fasi: la prima consiste nella creazione della mappa base e la seconda l’aggiunta degli indicatori.
Inoltre, programmando opportunamente la funzione popup, è possibile inserire ulteriori informazioni riguardo la posizione contrassegnata, per esempio codice scuola, Dirigente Scolastico, etc.
La classe icon permette di definire le caratteristiche dell’icona che rappresenta l’indicatore.
Infine è possibile utilizzare la funzione MarkerCluster() per raggruppare in un numero le Istituzioni Scolastiche, per poi visualizzarle in base allo zoom sull’area interessata.

### (./DATA/mappa_base.html)
