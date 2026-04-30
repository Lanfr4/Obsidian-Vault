[[0 Architettura degli Elaboratori e Laboratorio]]
## IMPORTANTE!!
Vogliamo cercare un formalismo che ci  permette di associare una espressione algebrica con una binaria, i valori 0 e 1 appartengono ai Naturali, nel mondi binario nn possiamo fare 1+1= 2, per questo bisogna utilizzare la ALGEBRA DI BOOLE

Definizione:
 	A = {A, +, ., ', 0, 1}
ciascun simbolo rappresenta:
A supporto dell' algebra
+, somma logica , OR
., prodotto logico , AND
', negazione, NOT
0 è elemento neutro rispetto a +, 1 è elemento neutro rispetto a .

Proprietà di Chiusura
	rispetto alla somma: a+b appartiene ad A per ogni a,b appartenente ad A
	rispetto al prodotto: a*b appartiene ad A per ogni a,b appartenente ad A
	rispetto alla complementazione: a' appartiene ad A per ogni a appartenente ad A
	congiunzione e disgiunzione sono commutative: a+b = b+a  a*b = b*a
	elemento neutro rispetto a +(0) ed elemento neutro rispetto a *(1): a+0 = a   a*1 = a
	proprieta distributiva: a+(b*c) = (a+b)* (a+c) o a*(b+c) = (a*b)+(a*c)
	per ogni a appartenente ad A esiste a' tale che: a+a'= 1 e a*a'= 0

Postulati (Huntington)
	congiunzione e disgiunzione sono commutative
	a + b = b + a a · b = b · a
	esistono un elemento neutro rispetto a + (indicato con 0) e un
	elemento neutro rispetto a · (indicato con 1) tali che:
	a + 0 = a a · 1 = a
	proprietá distributiva:
	a + (b · c) = (a + b) · (a + c) a · (b + c) = (a · b) + (a · c)
	per ogni a ∈ A esiste ed é unico un complemento a0tale che
	a + a
	0 = 1 a · a
	0 = 0
Variabili
Una variabile booleana è un simbolo che indica un qualsiasi elemento di A, il suo valore è specifico elemento di A, che denoteremo con le lettere dell' alfabeto , ora elencheremo una serie di proprietà:
	-**Associativa**: x+(y+z)=(x+y)+z x⋅(y⋅z)=(x⋅y)⋅z
- **Idempotenza**: x+x=x x⋅x=x
- **Elemento Nullo**: x+1=1 x⋅0=0
- **Assorbimento**: x+x⋅y=x x⋅(x+y)=x    
- **Semplificazione**: x+x′⋅y=x+y x⋅(x′+y)=x⋅y
- **Unicità del complemento**: x′ è unico.
- **Involuzione**: (x′)′=x
#### Leggi di De Morgan
(x+y)′=x′⋅y′
(x⋅y)′=x′+y′

 le espressioni logiche possono essere trasformate o "accorciate" usando delle regole (assiomi)
#### Teorema del Consenso
x⋅y+x′⋅z+y⋅z=x⋅y+x′⋅z
(x+y)⋅(x′+z)⋅(y+z)=(x+y)⋅(x′+z)

#### Principio di Dualità
Questa è una sorta di "regola dello specchio". Dice che ogni legge dell'algebra di Boole ha una sua "gemella". Se prendi un'uguaglianza vera e:

Scambi tutti i + (OR) con i · (AND).

Scambi tutti gli 0 con gli 1.
...ottieni un'altra uguaglianza che è altrettanto vera

#### Algebra di Commutazione
Si tratta di un algebra di Boole in cui il supporto é costituito da due soli valori 0 (Falso/Spento) e 1 (Vero/Acceso);

Un espressione booleana definita su un insieme di variabili
booleane X = {x1, x2, ...., xn} é definita dalle seguenti regole:
	• gli elementi del supporto sono espressioni
	• le variabili x1, x2, ...., xn sono espressioni
	• se g e h sono espressioni booleane, allora lo sono anche
	g + h, g · h e g'
	• non esistono altre espressioni oltre a quelle ottenute
	applicando iterativamente le regole precedenti
#### Funzioni Booleane
Funzione booleana di n variabili: relazione f : A^n → A che mette in corrispondenza gli elementi del dominio A^n = A × A × ....A con quelli del codominio:
	• funzione costante: f(x1, x2, ...., xn) = a, ∀a ∈ A
	• funzione proiezione: f(x1, x2, ...., xn) = xi,∀xi ∈ {x1, x2, ...., xn}
se g e h sono funzioni booleane a n variabili allora anche(g + h), (g · h) e (g') sono funzioni booleane:
	• (g + h)(x1, x2, ...., xn) = g(x1, x2, ...., xn) + h(x1, x2, ...., xn)
	• (g · h)(x1, x2, ...., xn) = g(x1, x2, ...., xn) · h(x1, x2, ...., xn)
	• (g')(x1, x2, ...., xn) = (g(x1, x2, ...., xn))0
#### Funzioni di Commutazione
Nell’algebra di commutazione A = {0, 1} (che viene indicato anchecome B) per cui:

f : {0, 1}^n → {0, 1}

Le funzioni di commutazione possono essere descritte tramite tabelle della veritá in cui si ha una riga per ciascuna configurazione delle variabili. La riga riporta il valore delle variabili e il corrispondente valore dif.
#### Letterali
Letterale: coppia (variabile, valore) di una variabile booleana (x ∈ {0, 1}) Nell’algebra di commutazione, si hanno 2 possibili letterali:
• (x, 1) indicato come x
• (x, 0) indicato come x'

Vedremo il loro utilizzo nella valutazione del costo di una rete
logica, con degli esempi( slide 29-32 di algebra.pdf)

#### Valutazione di una Espressione
La valutazione di una espressione rispetto a una configurazione  è il procedimento nel quale si sostituisce a ogni variabile il suo valore corrispondente utilizzando le regole dell' algebra di commutazione, bisogna farlo per ogni combinazione possibile, ottenendo cosi una tabella di verità in cui ogni espressione corrisponde una funzione

#### Semplificazione di una Espressione
Per semplificare una espressione utilizziamo le regole dell' algebra di commutazione, tenendo una espressione semplificata e uguale a quella di partenza;  

