202112091821
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Grafi

## Grafi orientati
[[Grafi orientati]]

## Grafi non orientati
[[Grafi non orientati]]

## Alberi
[[Alberi]]

### Cammini euleriani e cammini hamiltoniani

**Cammino Euleriano**
Dato un grafo non orientato connesso $G = (V, E)$, un **circuito euleriano** per $G$ è un circuito che **attraversa tutti gli archi in E una e una sola volta**. Analogamente, un **trail euleriano** (più comunemente chiamato *percorso euleriano*) è un trail per $G$ che attraversa tutti gli archi in $E$ una e una sola volta.

**Teorema**
Dato un grafo non orientato connesso $G$, esiste un **circuito euleriano** se e solo se ogni nodo ha **grado pari**. Esiste un **percorso euleriano** dal nodo $x$ al nodo $y$, con $x \neq y$, se e solo se dx e dy sono gli **unici gradi dispari**. ^7e5c5b

**Ciclo e path hamiltoniano**
Dato un grafo non orientato e connesso $G = (V, E)$, un **ciclo hamiltoniano** è un ciclo che **attraversa tutti i nodi in $V$ una e una sola volta** (tranne il nodo di inizio/fine). Un **path hamiltoniano** (più comunemente chiamato *cammino hamiltoniano*) è un path che **attraversa tutti i nodi in $V$ una e una sola volta**.

Si noti che un grafo può avere in generale **più cicli hamiltoniani**. Trovare un **path hamiltoniano** in sostanza consiste nel trovare una [[Calcolo Combinatorio|permutazione]] dei nodi in $V$ che dia luogo a un path. **L’apparente analogia con i circuiti euleriano purtroppo termina qui**: attraversare tutti gli archi una sola volta nel circuito euleriano, di contro ad attraversare tutti i nodi una sola volta nel ciclo hamiltoniano. Non esiste al momento una caratterizzazione per garantire l’esistenza o meno di un ciclo hamiltiniano in G, analoga a quanto enunciato nel [[#^7e5c5b|qua]]. Il ciclo hamiltoniano ha struttura combinatoria più complessa e sfuggente: trovare un ciclo hamiltoniano può risultare più arduo come compito e fa parte di una famiglia importante di problemi, chiamati NP-completi, la cui trattazione sarà argomento di un corso successivo.


### Il problema del commesso viaggiatore
Il famoso problema del commesso viaggiatore consiste nell’individuare, su di una mappa stradale in cui ogni strada è etichettata con la lunghezza in chilometri, un cammino che permetta al commesso viaggiatore di attraversare tutte le città e di tornare a casa percorrendo il minor numero possibile di chilometri. Il lettore può convincersi facilmente che questo problema può essere formulato come quello di trovare un ciclo hamiltoniano di peso minimo in un grafo pesato.

**Definizione**
Dato un grafo pesato $G = (V, E, L)$, il peso di un ciclo hamiltoniano $H = v_0, v_1, ... , v_k$ (quindi con v0 = vk) è la somma dei pesi degli archi attraversati da $H$:
$$peso(H) = \sum^k_{i=1}L(v_{i-1},v_i)$$

### Distanza

Una **distanza** (**metrica**) su un insieme $A$ è una funzione $d: A \times A \rightarrow R$ che soddisfa le seguenti proprietà per ogni $x, y, z \in A$:

1. $d(x,y) \geq 0$
2. $d(x,y) = 0\ se\ e\ solo\ se\ x=y$
3. $d(x,y) = d(y,x)$
4. $d(x, y) \leq d(x, z) + d(z, y)\ (disuguaglianza\ triangolare)$

Una [[Funzioni|funzione]] $d: A \times A \rightarrow R$ che soddisfa tutte queste proprietà tranne la [[Relazioni su un insieme|simmetria]]è chiamata **distanza quasi-metrica**

**Distanza su un grafo**
Sia $G = (V, E)$ un grafo non orientato connesso. Dati due nodi $x, y \in V$, la loro **distanza** $d(x, y)$ è la **[[Grafi orientati|lunghezza del walk]] più breve tra x e y**, chiamato **walk minimo** (o più comunemente cammino minimo).

**Distanza su un grafo induttivamente**
Sia $G = (V, E)$ un grafo non orientato connesso. Dati due nodi $x, y \in V$ , la loro distanza $d(x, y)$ è definita induttivamente come:
1. [Caso Base] $d(x,y) = 0$, se $x = y$;
2. [Passo induttivo] $d(x,y) = 1 + min\{d(z,y)\ |\ z \in vicini(x)\}$, altrimenti.

**Diametro**
Il **diametro** di un grafo $G$ (orientato o meno) è la **massima distanza tra coppie di nodi**:
$$diam(G) = max(\ \{d(x,y)\ |\ x,y \in V\}\ )$$
Nel caso degli alberi, si eredita la distanza dei grafi non orientati.

### Isomorfismo
Dati due qualunque grafi $G_1 = (V_1, E_1)$ e $G_2 = (V_2, E_2)$, dove $|V1| = |V2|$ e $|E1| = |E2|$, un isomorfismo tra $G_1$ e $G_2$ è una [[Biezioni|biiezione]] $f : V_1 \rightarrow V_2$ tra i loro nodi tale che, per ogni coppia di nodi $u, v \in V_1$, vale che $uv ∈ E_1$ se e solo se $f(u)f(v) \in E_2$ (cioè esiste il corrispondente arco in entrambi i grafi, oppure non esiste in entrambi di essi). In tal caso, $G_1$ e $G_2$ sono detti **isomorfi**.

---
### References
- [[Grafi orientati]]
- [[Grafi non orientati]]
- [[Alberi]]
- [[Calcolo Combinatorio]]
- [[Funzioni]]
- [[Relazioni su un insieme]]
- [[Biezioni]]