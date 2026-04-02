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

### Gate( tecnologia CMOS)
E' la soluzione, per far si che una rete di switch possa controllare gli switch appartenenti a un altra rete, ecco un esempio  applicato:

[IMMAGINE ]

Nel CMOS 