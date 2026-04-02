[[0 Architettura degli Elaboratori e Laboratorio]]
# Segnali
I segnali utilizzano grandezze binarie, ovvero 0 oppure 1, per codificare informazioni, che si possono distinguere in varie categorie:
	Analogico: il segnale assume valori all' interno di un insieme che varia nel tempo in modo continuo, e al' interno di certi insiemi può assumere valori infiniti
	Digitale: è un segnale discreto , può essere solo un finito numero di valori; se sono 2 è un segnale binario 
	 Sincrono: tipo di segnale che viene preso in considerazione ogni tot di Tempo(Clock)
	 Asincrono: tipo di segnale che può cambiare in qualsiasi momento

### Segnali Analogici
In teoria possono rappresentare una quantità infinita di informazioni, che pero sono limitati da:
accuratezza degli strumenti di Misura
	Rumore: disturbo di caratteristiche casuali da diverse origini che si sovrappone al segnale   originale

come riduciamo il rumore??

Per ridurre il rumore usiamo la DISCRETIZZAZIONE che è anche l' operazione per passare da ANALOGICO a DIGITALE, che si compone di 2 processi distinti:
	Campionamento : guardiamo il segnale in varie istanze, quindi lo  campioniamo, in intervalli regolari di tempo chiamati Periodo di Campionamento
	 Quantizzazione : Approssimiamo il valore che abbiamo campionato al valore numerico più vicino che lo rappresenta , durante questo processo il segnale ottiene maggiore tolleranza al rumore

Se decidiamo di utilizzare segnali in cui é significativo un numero finito di valori, rimane il  problema della scelta di questo numero(per esempio binario quindi 01 invece che decimale da 0 a 9); gli obbiettivi di questa scelta sono:
• robustezza rispetto al rumore
• caratteristiche del tipo di reti che possono elaborare tali segnali(Hardware)


### Segnali Binari
Segnali che assumono valore 0 oppure 1, scegliamo il segnale con n=2 perché quello più robusto e anche molto facile da costruire ci sono solo 2 stati o 0 oppure 1(più livelli più è complicato)

Se ci sono k livelli logici e n segnali si hanno k^n configurazioni possibili, inoltre il rapporto fra il numero di configurazioni binarie e k-narie per n segnali è (2/k)^n, ricordando che se aumentiamo k, quindi aggiungiamo livelli, è maggiormente possibile la presenza di rumore


### Segnali Asincroni
Segnale che può cambiare in qualsiasi momento , il problema sono i ritardi dei cavi che possono far leggere dati sbagliati alla destinazione,
per risolvere possiamo fare una operazione molto simile alla discretizzazione 

### Segnali Sincroni
Un segnale considerato valido solo in precisi istanti di tempo detto Clock, gli istanti di sincronizzazione devono corrispondere a intervalli di tempo in cui non avvengono transizioni;
La facilità dei progetto é il principale vantaggio dei sistemi sincroni, lo svantaggio é dato dalla velocità

### Asincrono vs Sincrono
Ecco i difetti/pregi di entrambi: 
	Velocità : 
		 Asincroni sono molto più veloci rispetto a quelli Sincroni, poiché  i primi possono cambiare quando vogliono 
		 Sincroni: Meno veloci poiché è presente il Clock
	Gestione dello Skew: 
		Asincroni (lo subiscono) perché vede i bit man mano che arrivano ( non avendo un Clock)  li può analizzare subito senza aspettare, ma alcune volte commette errori(dati fantasma) poiché vede bit in arrivo nn completi.
		 Sincroni ( lo gestiscono), avendo il segnale di clock ogni tot ns gli arriveranno dei bit completi da analizzare, però é generalmente più lento appunto per il Clock;

### Segnale di Clock
E' un segnale periodico binario, che coordina tutto il sistema,  un livello in cui i segnali sincroni devono avere un valore costante, il clock è il momento in cui il sistema legge i dati
