202112100904
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Grafi non orientati

**Definizione**
Un **grafo non orientato** $G = (V, E)$ consiste di un [[Insiemi|insieme]] finito $V$ e di un insieme $E \subseteq \mathcal{P}_2(V)$. Gli elementi di $V$ vengono detti **nodi** o vertici e gli elementi di $E$ vengono detti **archi** o lati.

### Grafo orientato assciato
Dato un grafo non orientato $G = (V, E)$, quindi $E \subseteq \mathcal{P}_2(V)$, il grafo orientato associato a $G$ è il grafo orientato $\widetilde{G} = (V, \widetilde{E})$ dove la relazione $\widetilde{E}$ è definita come
$$\widetilde{E} = \{(x, y) \in V \times V\ |\ \{x, y\} \in E\}: V \leftrightarrow V$$

### Vicinato e grado dei nodi
Le nozioni di vicinato e grado dei nodi risultano semplificate nel caso di grafi non orientati perché non si deve tener conto della direzione degli archi.

**Definizione**
Sia $G = (V, E)$ un grafo non orientato, quindi $E \subseteq \mathcal{P}_2(V)$. Due nodi $x, y \in V$ sono **vicini** o adiacenti se c’è un arco $x\ y \in E$: in tal caso tale arco si dice incidente a $x$ e $y$, i quali sono chiamati **estremi** dell’arco. Il vicinato di un nodo $x \in V$ è l’insieme $N(x) = \{y\ |\ x\ y \in E\}$. Il nodo $x$ è **universale** se è vicino a tutti i nodi (cioè $N(x) \cup \{x\} = V$ ), mentre è **isolato** se $N(x)$ è vuoto. Il grado di $x$ è definito come il numero di nodi a lui vicini, $dx = |N(x)|$; quindi $dx = 0$ se il nodo è isolato. Con $\Delta$ si rappresenta il grado massimo in $G$ (cioè $\Delta = max\{dx\ |\ x \in V\}$).

### Rappresentazione dei grafi non orientati
La rappresentazione di grafi non orientati mediante matrici e liste di adiacenza è del tutto simile a quella vista per i [[grafi orientati]]. Nella matrice di adiacenza di un grafo non orientato, l’elemento $A_{i,j}$ vale $1$ se $\{i, j\} \in E$ e $0$ altrimenti. Si noti che la matrice risultante è simmetrica: $A_{i,j} = 1$ se e solo $A_{j,i} = 1$; inoltre la diagonale è nulla: $A_{i,i} = 0$ per ogni $i \in V$ , perché non ci possono essere cappi. Nelle liste di adiacienza, per ogni nodo $i \in V$ l’elemento i-esimo dell’array $A$ è il vicinato di $i, A[i] = N(x)$.
Concludiamo questa sezione osservando che le definizioni di [[Grafi orientati|grafo etichettato e grafo pesato]] che abbiamo visto nel caso dei grafi orientati si possono adattare facilmente al caso di grafi non orientati.

### Cammini, cicli e connettività nei grafi non orientati
**Walk, trail, path**
Sia $G = (V, E)$ un grafo non orientato. Un **walk** in $G$ è una sequenza (di lunghezza arbitraria) di nodi $v_0, ..., v_k$, tali che $\{v_{i−1}, v_i\} \in E$ per ogni $i \in \{1, ..., k\}$.
La lunghezza di un walk, gli estremi, i nodi attraversati e gli archi attraversati sono definiti come per i [[grafi orientati]].
Trail e path sono analoghi a quello visti nei grafi orientati.

### Cicli nei grafi non orientati
I concetti di **walk chiuso**, **circuito** e **ciclo** sono definiti come per i [[grafi orientati]], così come anche le nozioni di **grafo ciclico** e **aciclico**. Però questi concetti acquiscono un valore leggermente diverso. In particolare, non è vero che l’esistenza di un walk chiuso implica l’esistenza di un circuito (e quindi di un ciclo), perchè il trail corrispondente a tale walk potrebbe avere lunghezza 0 e quindi non essere un circuito.

### Connettività
La connettività nei grafi non orientati è analoga a quella dei [[grafi orientati]]


---
### References
- [[Insiemi]]
- [[Relazioni]]
- [[Proprietà delle relazioni]]
- [[Relazioni su un insieme]]
- [[Grafi]]