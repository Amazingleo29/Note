202112091823
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Grafi orientati

**Definizione**
Un **[[Grafi|grafo]] orientato** è una [[Relazioni|relazione]] $E : V \leftrightarrow V$ su un [[Insiemi|insieme]] finito $V$ . Gli elementi di $V$ vengono detti **nodi** o vertici e gli elementi di $E$ vengono detti **archi** o lati. Per enfatizzare l’insieme dei nodi $V$ e l’insieme degli archi $E$, solitamente si scrive $G = (V, E)$ in cui $G$ è il modo in cui denotiamo un grafo.

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

**Disegnalo**
Prendi carta e penna XD.

**Matrice di adiacenza**
La rappresentazione più immediata per un grafo orientato $G = (V, E)$ con $n = |V|$ nodi è quella tabellare. 
**Definizione**
La **matrice di adiacenza** di $G$ è una matrice quadrata $A$ con $n$ righe e $n$ colonne, numerate da $0$ a $n − 1$, dove l’elemento $A_{ij}$ (in riga $i$ e colonna $j$) assume un valore in ${0, 1}$ con il seguente significato:
$$A_{ij} = 
\Bigg\{\begin{array}{}
1\ se\ l'arco\ (i,j) \in E;\\
0\ se\ l'arco\ (i,j) \notin E;\\
\end{array}$$ 
Esempio di matrice:

|       | a   | b   | c   |
| ----- | --- | --- | --- |
| **a** | 1   | 0   | 0   |
| **b** | 1   | 1   | 0   |
| **c** | 1   | 0   | 1   |

**Liste di adiacenza**
Per le reti sociali e per molti grafi che modellano strutture dal mondo reale (internet, reti neuronali, alberi genealogici, . . . ), spesso si utilizza una rappresentazione diversa che permette di risparmiare spazio se il grafo è sparso, cioè se il numero di archi è proporzionale al numero di nodi. A tal fine si utilizzano le liste di adiacenza.
**Definizione**
Le rappresentazione con liste di adiacenza di un grafo orientato $G = (V, E)$ è costituita da un array $A$ di $n = |V|$ insiemi in cui l’elemento i-esimo è il vicinato in uscita del nodo i ∈ V , cioè A[i] = N +(i).

### Grafi etichettati e pesati
Un **grafo orientato etichettato** è una tripla $G = (V, E, L)$ dove $L$ è una funzione $L:(V \cup E) \rightarrow D$ che associa ad ogni nodo e arco una etichetta presa da un certo dominio $D$ di valori (identità, date, località, distanze, ecc.). Nel caso che $D$ sia un valore numerico (soliltamente un numero reale), il grafo etichettato si chiama **pesato** e ciascuna etichetta viene indicata come **peso** (dell’arco o del nodo).

### Cammini, cicli e connetività nei grafi

**Walk**
Sia $G = (V, E)$ un grafo orientato. Un **walk** $P$ in $G$ è una sequenza di nodi $P = v_0, ..., v_k$ di lunghezza arbitraria (con $k \in N$), tali che $(v_{i−1}, v_i) \in E$ per $i \in \{1, ..., k\}$. In questo caso $P$ è un walk di lunghezza $k$. Le coppie $(v_{i−1}, v_i) \in E$ sono detti gli archi **attraversati** da $P$ ed i nodi $v_0, ..., v_k$ sono detti i nodi attraversati da $P$. Si dice inoltre che $P$ è un walk da $v_0$ a $v_k$, o che $P$ inizia con il nodo $v_0$ e termina nel nodo $v_k$. I nodi $v_0$ e $v_k$ sono chiamati gli **estremi** di $P$. Si noti che se $k = 0$, il walk ha lunghezza $0$ ed è costituito dal solo nodo $v_0$. La **lunghezza** di un walk è data dal numero di archi che attraversa.

**Trail**
Un walk $P$ è detto un **trail** se attraversa ogni arco in $E$ al più una volta.

**Path**
Un trail è detto un **path** se attraversa ogni nodo in $V$ al più una volta.

### Cicli nei grafi orientati

Un walk **P** è detto **chiuso** se i suoi estremi sono uguali (cioè $v_0$ = $v_k$) e se ha lunghezza $> 0$. Un **walk chiuso** che è un **trail** è detto **circuito**. Un **circuito** che è anche un **path** è detto un **ciclo**, facendo ovviamente eccezione per gli estremi (cioè gli estremi ERRATA vengono contati due volte). In altre parole un ciclo è un circuito $v_0, ..., v_k$ (con $v_0 = v_k$) tale che $v0, ..., v_k−1$ è un path.

### Connettività

**Grafo fortemente conneso**
Un grafo orientato $G = (V, E)$ è fortemente connesso se per ogni coppia di nodi $(u, v) \in V \times V$ esiste un walk da u a v

**Componente fortemente conessa**
Sia $G = (V, E)$ un grafo orientato. Una componente fortemente connessa di $G$ è un sottoinsieme non vuoto di nodi $U \subseteq V$ tale che:
1. Per ogni coppia di nodi $(x, y) \in U \times U$ esiste un walk da $x$ a $y$
2. Se $U_0 \subseteq V$ soddisfa la proprietà 1. e $U \subseteq U_0$ , allora $U = U_0$ 

La prima condizione richiede che in una componente connessa, presi due nodi arbitrari $x$ e $y$, ci sia sempre un walk da $x$ a $y$ e viceversa. La seconda condizione invece richiede che ogni componente fortemente connessa sia massimale, cioè aggiungendo un nodo esterno ad essa la prima condizione deve essere violata.

### DAG (Directed Acyclic Graph)
**Definizione**
Un **grafo o rientato aciclico** è detto **DAG** (dall’inglese directed acyclic graph). In un DAG i nodi con grado d’ingresso zero sono detti **sorgenti** e quelli con grado d’uscita zero sono detti **pozzi**.

Se $G = (V, E)$ è un DAG, allora $E^*$ è una relazione d’[[Relazioni su un insieme|ordinamento parziale]].

**Ordinamento topologico**
Dato un DAG $G = (V, E)$, un ordinamento topologico di $G$ è una biiezione $\eta : V \rightarrow n = \{0, 1, . . . , n − 1\}$ tale che 
$$per\ ogni\ arco\ (u, v) \in E\ vale\ \eta(u) < \eta(v).$$
In altre parole, se disponiamo i vertici lungo una linea orizzontale in base alla loro numerazione η, in ordine crescente, otteniamo che gli archi risultano tutti orientati da sinistra verso destra.

---
### References

- [[Insiemi]]
- [[Relazioni]]
- [[Proprietà delle relazioni]]
- [[Relazioni su un insieme]]