[[0 Architettura degli Elaboratori e Laboratorio]]
# Codifica Binaria delle Informazioni
Come codice binario(BlockCode) si intende una funzione f : {0,1}^n ->J ; dove J rappresenta un insieme M di informazioni
(foto su slide del 26/02/2026 slide n°2)
condizioni per cui i codici binari sono banali:
alcune configurazioni possono essere inutilizzate
più di una configurazione può rappresentare più informazioni
l' utilizzo di n bit è una restrizione , in quanto a informazioni diverse posso essere associate parole di lunghezza diversa

Il numero di configurazioni binarie deve essere maggiore o uguale al numero di informazioni(M) da codificare:
 	2^n>=M
quindi:
 	$$n \ge \lceil \log_2 M \rceil$$

Fissato n, numero possibili di codici C, è dato dal numero delle configurazioni binarie 2^n prese a M alla volta:
 	C = 2^n(2^n -1).....(2^n -M+1)
che possiamo riscrivere come:
 	C = (2^n)!/(2^n - M)!

Nella codifica delle informazioni all' interno delle CPU e altri sistemi digitali si utilizzano le seguenti codifiche:
	complemento a 2 per gli interi
	virgola mobile o fissa per reali
	ASCII(8bit) o ISO(16bit) per i caratteri

All' infuori di questo ambito diverse codifiche servono per rappresentare diversi tipi di codici; l' operazione di passaggio da un codice all' altro viene definita Conversione o Transcodifica


