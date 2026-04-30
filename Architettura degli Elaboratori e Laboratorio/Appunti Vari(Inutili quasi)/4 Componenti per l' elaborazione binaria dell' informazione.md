[[0 Architettura degli Elaboratori e Laboratorio]]
# Porte Logiche
Una porta logica è il "mattone" fondamentale dell'elettronica digitale. È un piccolo circuito fisico che prende in ingresso uno o più segnali binari (composti solo da 0 e 1) e restituisce un segnale in uscita basato su una precisa regola logica (chiamata algebra di Boole).

In termini più semplici: è come un vigile urbano che decide se far passare o meno la corrente elettrica (il segnale) in base a delle regole stabilite.

Come funziona?
Le porte logiche lavorano con due soli stati:
1 (Vero / Alto): C'è corrente.
0 (Falso / Basso): Non c'è corrente.

Ecco le principali Porte Logiche, e il risultato che portano
![[Porte Logiche.png|470]]
altre porte logiche
![[Pasted image 20260317101643.png|469]]
## Livello Switch
A livello Switch la tecnologia più diffusa è  il CMOS, lo switch praticamente è un interruttore che serve a far cambiare lo stato, da 0 a 1, appunto è un componente binario, nella CMOS ci sono 2 modalità in cui può avvenire la connessione:
	SERIE: (praticamente un AND)
	PARALLELO: (praticamente un OR)

La rappresentazione logica si divide in:
POSITIVA: cioè AND e OR funzionano normalmente
NEGATIVA: è l' inverso della positiva( ovvero per l' OR vale la regola dell' AND e viceversa)

### Reti di Switch
Il Concetto di "Rete di Switch" in ambito circuitale, una rete complessa è costituita da molteplici interruttori collegati tra loro. Per comprendere il comportamento globale della rete (cioè: "quando passa la corrente?"), non si analizza l'intero circuito simultaneamente, ma lo si scompone in sottosistemi piu piccoli. Questi sottosistemi seguono due topologie fondamentali: la connessione in Serie e la connessione in Parallelo.


### Dettagli sui Transistori (Livello Switch)

Nella tecnologia CMOS, il componente elementare più semplice al livello logico non è la porta logica intera, ma il transistore, che funziona come un interruttore (switch). Un segnale binario controlla il suo stato (ON/OFF).

Esistono due tipi fondamentali di transistori:

- **Transistore di tipo n:** È spento (OFF) quando riceve uno 0 ed è acceso (ON) quando riceve un 1.
- **Transistore di tipo p:** Funziona al contrario; è acceso (ON) quando riceve uno 0 ed è spento (OFF) quando riceve un 1.
    

**Principio di Dualità:** Riguarda il modello logico dei sistemi fisici. Utilizzando lo stesso tipo di logica, le reti in serie e in parallelo realizzano funzioni duali (come AND e OR). In pratica, una serie è ON se entrambi gli switch sono ON, mentre un parallelo è ON se almeno uno o l'altro degli switch è ON.

### Costruzione Fisica delle Porte (Reti Pull-up e Pull-down)

Le reti composte solo da semplici switch presentano un problema elettrico: gli switch non sono ideali e possiedono una resistenza in serie. Se ci sono troppi switch collegati, l'informazione elettrica si degrada.

La soluzione nella tecnologia CMOS è usare una rete di switch per controllare gli switch di un'altra rete, fornendo un guadagno che "rinforza" i segnali. Si utilizzano le costanti 1 ($vdd$) e 0 ($gnd$) e due reti con stati complementari:

- **Rete di Pull-down:** Costruita con transistori di tipo n. Pilota uno 0 in uscita (ad esempio, in una porta NAND lo fa quando entrambi gli ingressi valgono 1).
    
- **Rete di Pull-up:** Costruita con transistori di tipo p. Pilota un 1 in uscita (ad esempio, in una porta NAND lo fa quando almeno uno degli ingressi vale 0).
    

### Aspetti Tecnologici: Costo e Ritardo

I circuiti sono realizzati integrando milioni di porte logiche su materiali semiconduttori (es. silicio) usando una tecnologia planare (i dispositivi non si possono sovrapporre, ma le interconnessioni sì, su livelli diversi).

- **Costo:** È proporzionale all'area utilizzata sul circuito integrato. L'area dipende dal numero di transistori (e quindi dal numero di ingressi delle porte) e dalle interconnessioni necessarie.
- **Ritardo di Propagazione:** I cambiamenti dei valori in ingresso non si riflettono istantaneamente sull'uscita. Poiché l'informazione viaggia tramite tensioni, è necessario muovere delle cariche fisiche, il che richiede tempo. Questo ritardo è proporzionale al numero di transistori in serie e al carico capacitivo, ed è un fattore critico per le prestazioni di un sistema digitale.
    

### Reti Logiche Combinatorie

Una rete logica combinatoria è un insieme di porte logiche interconnesse per realizzare una funzione specifica. Devono rispettare due regole ferree:

1. Le uscite di due gate non devono **mai** essere connesse insieme.
2. Non devono esistere percorsi (cammini) ciclici all'interno della rete.

Lo studio di queste reti si divide in due processi basati sull'algebra di commutazione:

- **Analisi:** È il processo che parte dalla rete fisica (o dal suo schema) e fornisce la funzione matematica corrispondente. Si parte dando un nome agli ingressi e si calcolano iterativamente le uscite di ogni gate fino ad ottenere la tabella di verità finale. Questo processo ha un costo proporzionale a $2^n$ (dove $n$ è il numero di ingressi).
- **Sintesi:** È il processo inverso. Parte da una funzione matematica e dagli obbiettivi di progetto (costo, ritardo) per produrre la rete logica. Tramite un algoritmo, si assegnano livelli di priorità alle parentesi e agli operatori per capire in che ordine disegnare e collegare le porte logiche.

**Il ruolo del Fan-out:** Il "fan-out" indica quando l'uscita di una singola porta logica pilota gli ingressi di più porte successive (fan-out > 1).

- _Vantaggio:_ Riduce il numero totale di porte logiche necessarie e, di conseguenza, il costo della rete.
- _Svantaggio:_ Aumenta il ritardo di propagazione della rete. Nella sintesi, richiede di cercare sotto espressioni comuni prima di disegnare il circuito.