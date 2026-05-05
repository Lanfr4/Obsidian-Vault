# Reti Logiche
Esistono 2 tipi di Reti Logiche:
	Combinatorie(senza memoria e tempo): Queste reti Logiche possono essere risolte in 2 modalità:
		Metodo di Karnaugh;
		 Sintesi(si lege il circuito con le porta AND, OR ecc..);
	 Sequenziali(con memoria e tempo): le possiamo risolvere con un solo metodo:
		 FSM(Diagramma degli Stati);

## Analisi e Sintesi delle Reti Logiche Combinatorie
Ecco qua gli step  per semplificare una rete combinatoria con Karnaugh:
	1)Individuare gli 1 nella tabella di Verità e raccoglierli con altri 1 in gruppi di dimensioni di potenze di 2(1,2,4,8,16) ; inserendo anche i dont' care se necessario "-"( !!!! i - possono essere raccolti in gruppi di 1 se è presente almeno un 1 ), se nn vengono raccolti diventano automaticamente 0.
	 2)Poi andare a vedere dove sono gli 1 e come gli indici ab e cd cambiano in base alla posizione degli 1 nella tabella nel seguente modo:
		 Se cambiano da 0 a 1 , o viceversa, nn vanno inseriti;
		 Se rimangono invariato a 0 mettiamo l'apice ' (che vuol significare NEGATIVITA')
		 Se rimangono invariati ad 1 si scrive la lettere normalmente

### TRUCCO
Quando si raggruppano gli 1 in base alla dimensione del gruppo sappiamo che:
	Se si raccolgono 2 celle si elimina 1 lettera
	Se si raccolgono 4 celle si eliminano 2 lettere
	Se si raccolgono 8 celle si eliminano 3 lettere
### Sintesi
Per Risolvere le Reti Logiche tramite sintesi bisogna semplicemente vedere l' input da ogni punto della mia rete e associarli con altri tramite AND,OR, ecc.. per far si che risulti un output 0 oppure 1;
qui sotto c'è la tabella di verità per tutte le componenti più importanti:
 
## Analisi e Sintesi delle Reti Logiche Sequenziali
Per risolvere qualsiasi esercizio di reti logiche sequenziali, segui questa sequenza (puoi impararla a memoria):

| **Step** | **Nome del Passaggio**          | **Cosa devi fare in pratica**                                                                                              |
| -------- | ------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **1**    | **Analisi del problema**        | Identifica il numero di bit, cosa determina l'uscita (1 o 0) e quando la macchina deve "resettarsi".                       |
| **2**    | **Diagramma degli Stati (FSM)** | Disegna i cerchi ($S_0, S_1...$) e le frecce con Input/Output. (È quello che abbiamo imparato a fare!).                    |
| **3**    | **Tabella delle Transizioni**   | Traduci il diagramma in una tabella: _Stato Presente_, _Input_ $\rightarrow$ _Stato Futuro_, _Output_.                     |
| **4**    | **Codifica**                    | Assegna un valore binario agli stati ($S_0=00, S_1=01...$).                                                                |
| **5**    | **Sintesi (Karnaugh)**          | Usa le mappe di Karnaugh per trovare l'equazione del "Prossimo Stato" e dell' "Output" basandoti sulla tabella al punto 3. |
| **6**    | **Disegno del Circuito**        | Disegna porte AND, OR, NOT e i Flip-Flop (collegati secondo le equazioni trovate).                                         |
# Prossimo Argomento
