[[0 Architettura degli Elaboratori e Laboratorio]]

# Forme Canoniche
Cosa sono?
Sono espressione che sono uniche, ovvero che un solo risultato(tabella di verità) puo essere data solamente da una sola funzione
Come?
Possiamo affrontare il problema in due modi:
	Utilizziamo alcune proprietà dell' algebra di commutazione(Teorema dell' Espazione di Shannon)
	 Utilizziamo il calcolo delle proposizioni
### 1. Forme Canoniche (Il punto di partenza)

Per convertire una funzione logica (descritta ad esempio da una tabella di verità) in un'espressione matematica univoca, si utilizzano le forme canoniche.

- **Minitermini:** Sono termini prodotto (AND) in cui compaiono tutte le n variabili della funzione, in forma vera o complementata. Essi corrispondono alle righe della tabella di verità in cui la funzione vale 1.
- **Prima Forma Canonica (SP o SOP - Somma di Prodotti):** È la disgiunzione (somma OR) di tutti i mintermini per i quali la funzione vale 1. La formula è f=∑ i∣fi​=1​mi​.
- **Maxtermini:** Sono termini somma (OR) in cui compaiono tutte le n variabili, e corrispondono alle righe della tabella di verità in cui la funzione vale 0.
- **Seconda Forma Canonica (PS o POS - Prodotto di Somme):** È la congiunzione (prodotto AND) di tutti i maxtermini per i quali la funzione vale 0.
- **Costo:** Fissato un ordine delle variabili, queste espressioni sono uniche. Tuttavia, creano reti molto costose, con un costo proporzionale a 2n.

### 2. Ottimizzazione e Valutazione del Costo

Poiché le forme canoniche sono "costose" in termini di spazio fisico sul circuito, l'obiettivo è semplificarle esplorando espressioni equivalenti.
Per stimare il costo di una rete prima ancora di realizzarla fisicamente, si usano diverse metriche:

- Il conteggio puro del numero di gate (porte logiche).
- Il numero di letterali presenti nell'espressione matematica.
- La somma dei gate pesata sul numero dei loro ingressi (considerando anche i gate "nascosti" dalle parentesi).
- Il numero totale di termini prodotto o termini somma.
- **Criticità:** Queste metriche spesso ignorano il costo delle interconnessioni fisiche e si complicano quando una rete sfrutta un fan-out maggiore di 1, perdendo la corrispondenza uno-a-uno tra espressione e rete.
    

### 3. Forme Normali e Sintesi a Due Livelli

Le forme normali SP e PS sono espressioni semplificate (non necessariamente uniche) che corrispondono fisicamente a reti logiche a 2 livelli. Sono molto interessanti per ragioni tecnologiche di fabbricazione.
- **Metodi di sintesi:** Possono essere "esatti" (trovano la rete dal costo minimo assoluto) o "euristici" (trovano un minimo locale riducendo i tempi di calcolo).
- **Mappe di Karnaugh:** Sono un metodo euristico e grafico utilizzato per ottimizzare funzioni fino a un massimo di 6 variabili di ingresso.
- **Implicanti e Implicati:** Un implicante (per reti SP) è un termine prodotto che, se vale 1, rende la funzione sicuramente vera. Un implicato (per reti PS) è un termine somma che garantisce che la funzione valga 0. Quando non possono essere ulteriormente espansi, vengono definiti "primi".
- **Espansione:** Tramite le regole dell'algebra (come l'idempotenza P+P=P) si possono semplificare i termini. Si sfruttano configurazioni binarie (es. {0,1,−}) e si misurano le Distanze di Hamming. Se due termini distano 1 (cioè differiscono per una sola variabile), possono essere espansi e semplificati eliminando quella variabile.

