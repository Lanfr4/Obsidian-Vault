[[0 Architettura degli Elaboratori e Laboratorio]]
## Come semplificare Reti Combinatorie con Karnaugh
Ecco qua gli step  per semplificare una rete combinatoria con Karnaugh:
	1)Individuare gli 1 nella tabella di Verità e raccoglierli con altri 1 in gruppi di dimensioni di potenze di 2(1,2,4,8,16) ; inserendo anche i dont' care se necessario "-"( !!!! i - possono essere raccolti in gruppi di 1 se è presente almeno un 1 ), se nn vengono raccolti diventano automaticamente 0.
	 2)Poi andare a vedere dove sono gli 1 e come gli indici ab e cd cambiano in abse alla posixione degli 1 nella tabella nel seguente modo:
		 Se cambiano da 0 a 1 , o vicevesa, nn vanno inseriti;
		 Se rimangono invariato a 0 mettiamo l'apice ' (che vuol significare NEGATIVITA')
		 Se riamngono invariati ad 1 si scrive la lettere normalemente

### TRUCCO
Quando si raggruppano gli 1 in base alla dimensione del gruppo sappiamo che:
	Se si raccolgono 2 celle si elimina 1 lettera
	Se si raccolgono 4 celle si eliminano 2 lettere
	Se si raccolgono 8 celle si eliminano 3 lettere



# Reti Logiche 
Per Risolvere le Reti Logiche ci sono 2 metodi:
	1) 