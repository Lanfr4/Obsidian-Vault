## 1. Sottospazi Vettoriali 🧊

**Obiettivo:** Capire se un insieme di vettori (definito da equazioni) è un "ambiente chiuso".

- **Test 1 (Vettore Nullo):** Sostituisci tutti gli $x, y, z$ con $0$. L'equazione fa $0$? Se c'è un numero da solo (es. $+5$), **non** è un sottospazio.
    
- **Test 2 (Somma):** Se prendi due vettori generici che soddisfano l'equazione, la loro somma la soddisfa ancora?
    
- **Test 3 (Prodotto):** Se moltiplichi il vettore per $k$, l'equazione resta uguale a $0$?
    
- **Trucco rapido:** Se vedi $x^2, |x|, \sin(x)$ o termini noti ($\neq 0$), **NON** è un sottospazio.
    

---

## 2. Indipendenza Lineare (L.I.) 🚀

**Obiettivo:** Capire se ci sono "doppioni" o vettori inutili che possono essere scritti usando gli altri.

- **Il Test del Sistema:** Scrivi la combinazione lineare $x\vec{v_1} + y\vec{v_2} + z\vec{v_3} = \vec{0}$.
    
- **Risoluzione:** Se l'unica soluzione possibile è che tutti i coefficienti siano zero ($x=0, y=0, z=0$), allora sono **Linealmente Indipendenti**.
    
- **Segnale di pericolo:** Se trovi che un vettore è multiplo di un altro (es. $(1,2)$ e $(2,4)$), sono **Dipendenti**.
    

---

## 3. Generatori 🏗️

**Obiettivo:** Capire se con quei vettori puoi "costruire" ogni punto dello spazio (es. tutto $\mathbb{R}^3$).

- **Il Test del Vettore Generico:** Scrivi $x\vec{v_1} + y\vec{v_2} + z\vec{v_3} = (a, b, c)$.
    
- **Verifica:** Il sistema è risolvibile per **qualsiasi** valore di $a, b, c$?
    
    - Se sì $\rightarrow$ Sono generatori.
        
    - Se ottieni un'impossibilità (come abbiamo visto prima: $x+y=a$ e $x+y=c$), allora **non** generano tutto lo spazio.
        
- **Regola d'oro:** Per generare $\mathbb{R}^n$ servono **almeno** $n$ vettori. (Es: in $\mathbb{R}^3$ te ne servono almeno 3).
    

---

## 4. Base 💎

**Obiettivo:** È il "set perfetto". Non ne mancano e non ce ne sono in più.

Un insieme di vettori è una **Base** se e solo se valgono contemporaneamente queste due condizioni:

1. Sono **Linealmente Indipendenti** (non ci sono sprechi).
    
2. Sono **Generatori** (coprono tutto lo spazio).
    

> **Scorciatoia:** Se sei in $\mathbb{R}^n$ e hai esattamente $n$ vettori:
> 
> - Se sono L.I., allora sono automaticamente anche una base.
>     
> - Se sono generatori, allora sono automaticamente anche una base.
>