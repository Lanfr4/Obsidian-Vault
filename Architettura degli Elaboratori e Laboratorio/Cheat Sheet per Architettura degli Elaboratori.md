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
![[brave_screenshot_classroom.google.com.png]] 
## Analisi e Sintesi delle Reti Logiche Sequenziali
Questo tipo di Reti si risolve tramite FSM, per farlo si svolgono i seguenti step:
