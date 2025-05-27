L'algoritmo in questione è un indicatore adattivo di trading concepito per delineare una strategia basata su volumi e regressione del trend.

- Il codice si ancora automaticamente al pivot ideale in un range che va da 400 fino a 1500 candele e continua a riadattarsi in base alle condizioni di mercato ancorandosi al pivot più idoneo a delineare il trend.
- Trova gap in apertura mercato e inefficienze a mercato
- Delinea livelli dinamizzati di supporto e resistenza concepiti su uno studio dei livelli storici di vix per evitare aperture rapide di posizioni in fasi critiche di mercato
- Analizza con un particolare volume profile corpo e spike delle candele raddoppiando il peso degli spike in modo da aumentare la precisione dell’indicatore. 
- Ricava una zona volumetricamente interessante attorno al poc in base ad una % che si modifica in base all’estesione dei livelli di Fibonacci interni al box di trade (il box di trade è diviso in 5 livelli e cerco di mantener stabili livelli di volume   intorno ai 3 livelli di Fibonacci per evitare compressioni o decompressioni delle zone volumetricamente interessanti).
- Studio linear regression e indicatore di Pearson (linearità del trend) per gestione di diversi scenari.
- Market Analisi - Volume analisi - Scenario Analisi

In base all’analisi svolta viene stabilita la successiva posizione.


Iterazioni di posizione.
Posizioni Break: (Tutte mutualmente escluse)
-Break
-Siffredi
Posizioni Mid: (Tutte mutualmente escluse)
-Bot_Liq
-Val
-Poc
-Vah
-Poc2
-Actual pivot over bot
Posizioni Bot: (Mutualmente escluse)
-Bot Liq x2 target differenziati
-Old Sup x2 target differenziati
Posizioni cover
-Cover 1 x2 target differenziati
-Cover 2 x2 target differenziati
-Cover 3x 2 target differenziati
-Cover 4 x2 target differenziati
-Posizione Cover in modalità Siffredi che sostituisce 1 dei due livelli di cover sottostanti.

Working progress:

- Studio dei dati storici per ottimizzazione delle deviazioni standard della linear regression
- Ottimizzazione della linear regression con inserimento di una curva esponenziale campionata sullo storico dei dati per evitare falsi segnali
