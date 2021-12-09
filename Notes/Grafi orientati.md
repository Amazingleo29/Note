202112091823
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Grafi orientati

**Definizione**
Un **[[Grafi|grafo]] orientato** è una relazione $E : V \leftrightarrow V$ su un [[Insiemi|insieme]] finito $V$ . Gli elementi di $V$ vengono detti **nodi** o vertici e gli elementi di $E$ vengono detti **archi** o lati. Per enfatizzare l’insieme dei nodi $V$ e l’insieme degli archi $E$, solitamente si scrive $G = (V, E)$ in cui $G$ è il modo in cui denotiamo un grafo.

### Vicinato e grado
**Vicini**
Due nodi $x, y \in V$ sono adiacenti o vicini se c’è un arco che li collega (quindi $(x, y) \in E$ o $(y, x) \in E$ )

**Vicinato**
Il **vicinato in uscita** di un nodo $x \in V$ è l’insieme $N^+(x) = \{y\ |\ (x, y) \in E\}$. Analogamente, il **vicinato in ingresso** di un nodo $x \in V$ è l’insieme $N^−(x) = \{y\ |\ (y, x) \in E\}$.

**Grado**
Il **grado di uscita** di x è definito come la cardinalità del suo vicinato di uscita, $d^+_x = |N +(x)|$, mentre il suo **grado di ingresso** è definito come $d^−_x = |N −(x)|$.

È interessante notare che le quattro principali [[proprietà delle relazioni]] corrispondo esattamente a condizioni sui gradi d’ingresso e d’uscita di tutti i nodi:
- 1. $E : V \leftrightarrow V$ è totale se e solo se per ogni nodo $x \in V$ vale $d^+_x \geq 1$
- 2. $E : V \leftrightarrow V$ è univalente se e solo se per ogni nodo $x \in V$ vale $d^+_x \leq 1$
- 3. $E : V \leftrightarrow V$ è iniettiva se e solo se per ogni nodo $x \in V$ vale $d^-_x \leq 1$
- 4. $E : V \leftrightarrow V$ è surgettiva se e solo se per ogni nodo $x \in V$ vale $d^-_x \geq 1$

### Rappresentazione dei grafi orientati

1. **Disegnalo**
2. **Matrice di adiacenza**
La rappresentazione più immediata per un grafo orientato $G = (V, E)$ con $n = |V|$ nodi è quella tabellare. 
**Definizione**
La **matrice di adiacenza** di $G$ è una matrice quadrata $A$ con $n$ righe e $n$ colonne, numerate da $0$ a $n − 1$, dove l’elemento $A_{ij}$ (in riga $i$ e colonna $j$) assume un valore in ${0, 1}$ con il seguente significato:
$$A_{ij} = 
\Bigg\{\begin{array}{}
1\ se\ l'arco\ (i,j) \in E;\\
0\ se\ l'arco\ (i,j) \notin E;\\
\end{array}$$ 
- Esempio di matrice:
- 
|       | a   | b   | c   |
| ----- | --- | --- | --- |
| **a** | 1   | 0   | 0   |
| **b** | 1   | 1   | 0   |
| **c** | 1   | 0   | 1   |

3. **Liste di adiacenza**
Per le reti sociali e per molti grafi che modellano strutture dal mondo reale (internet, reti neuronali, alberi genealogici, . . . ), spesso si utilizza una rappresentazione diversa che permette di risparmiare spazio se il grafo è sparso, cioè se il numero di archi è proporzionale al numero di nodi. A tal fine si utilizzano le liste di adiacenza.
**Definizione**
Le rappresentazione con liste di adiacenza di un grafo orientato $G = (V, E)$ è costituita da un array $A$ di $n = |V|$ insiemi in cui l’elemento i-esimo è il vicinato in uscita del nodo i ∈ V , cioè A[i] = N +(i).


---
### References