# Qicksort
- Non stabile

- Ordina in loco

- Partiziono l'array in due e chiamo ricorsivamente quicksort sulle due partizioni fino ad arrivare ad array lunghi 1

- Invariente --> [Slide 30 Rand_QS] proprietà che non varia durante l'esecuzione del codice, si usa di solito per dimostrare la correttezza del programma 

- Complessità  [Slide 34 Rand_QS]
	- Caso Ottimio Teta(nlogn)
	- Caso Medio circa Teta(n^2)
	- Caso Pessimo (Array già ordinato) Teta(n^2)

# Random Quicksort
- piveaut casuale  
- Complessità
	- Costo medio 

- Analisi del caso medio
	- casi favorevoli (è all' "esterno") n/4
		casi favorevoli (è all' "interno") n/2
	  	casi favorevoli (è all' "esterno") n/4 
	-	T(n) = T(n-1) +O(n) --> continua sulle slide [Rand_QS]