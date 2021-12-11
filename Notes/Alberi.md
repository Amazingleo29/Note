202112101057
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Alberi

Un **albero** è un **[[Grafi non orientati|grafo non orientato]] connesso, aciclico e non vuoto**. I nodi alle estremità, ovvero i nodi di grado 1, vengono detti **foglie** mentre gli altri nodi sono talora indicati come **interni**. Una **foresta** è un grafo non orientato e aciclico (eventualmente non connesso). Ogni **componente connessa** di una foresta **è un albero**.

### Alberi radicati

Un albero radicato $G = (V, E, r)$ è costituito da un albero $G = (V, E)$ e da un suo nodo $r \in V$ chiamato **radice** $r$. Dato un nodo $y \neq r$, i nodi lungo l’unico cammino che collega $y$ a $r$ vengono chiamati gli **antenati** di $y$, e il primo (quello adiacente a $y$) è detto il **genitore** di $y$. Simmetricamente, $y$ viene detto **discendente** dei suoi antenati, e **figlio** del suo nodo genitore.
Dato un albero radicato $G = (V, E, r)$ e un nodo $r' \in V$ , il **sottoalbero** di $G$ con radice $r'$ è l’albero radicato $G' = (V', E', r' )$, in cui $V' \subseteq V$ contiene $r'$ e tutti i suoi discendenti in $G$, e $E' \subseteq E$ contiene tutti gli archi di $G$ tra nodi in $V'$ (formalmente, $E' = E \cap \mathcal{P}_2(V')$).

### Alberi ordinali e cardinali
Un **albero radicato** si dice ordinale se per ciascun nodo interno è definito un [[Relazioni su un insieme|ordinamento totale]] tra i suoi figli. Un albero radicato si dice **cardinale** o **k-ario** se ogni nodo interno ha esattamente $k$ figli, alcuni dei quali possono essere vuoti (indicati con $null$). I figli sono numerati e chiamati figlio 0, figlio 1, . . . , figlio k − 1. L’albero è **completo** se ogni nodo interno ha tutti e $k$ i figli non vuoti. Un caso speciale e molto importante è quando k = 2: in tal caso l’albero viene detto **binario**, dove il primo figlio viene chiamato **figlio sinistro** e il secondo figlio viene chiamato **figlio destro**.

**Profondità**
Dato un albero radicato, la **profondità** di un nodo $x$ è la sua distanza $d(x, r$) dalla radice $r$, e l’**altezza** di $x$ è la massima distanza tra 	$x$ e le sue foglie discendenti. L’**altezza** di un albero radicato è l’altezza della sua radice. Un **albero cardinale** si dice **pieno** se è completo e le foglie sono tutte alla stessa distanza dalla radice.


---
### References