202112041319
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Automi
**Definizione**: Sia A un [[alfabeto]]. Un automa sull’alfabeto A è una tripla $\mathcal{A}$ = (S, T, F) dove:

- $S$ è un insieme, detto **insieme degli stati**
- $T \subseteq (A \times S) \times S$  è una relazione in $Rel(A \times S, S)$, detta **relazione di transizione**, che associa ad ogni lettera dell’alfabeto $a \in A$ e ad ogni stato di partenza $x \in S$ zero o più stati di arrivo
- $F \subseteq S$ è l’insieme degli **stati finali** (anche detti stati di accettazione)

L’automa $\mathcal{A}$ si dice a **stati finiti** se l’insieme degli stati S è finito.

Intuitivamente, gli elementi di S sono tutti gli stati, e quelli di F sono gli stati di accettazione. Un elemento $((a, x), y) \in (A \times S) \times S$  rappresenta una transizione che porta l’automa dallo stato di partenza x allo stato di arrivo y leggendo il simbolo $a \in A$.

**Raggiungibillità**: 
per ogni stringa $w \in A^*$, si definisce la relazione $T_w \in Rel(S,S)$

1. [Clausola Base] $T_\varepsilon = id_S$
2. [Clausola Induttiva] $T_{aw} = T_a;T_w$
  
Se $(x,y) \in T_w$ si dice che lo stato y è **Raggiungibile** da x con la stringa w o che x può raggiungere y con la stringa w.

**Lingguaggio accettato**: Sia $\mathcal{A}$ = (S, T, F) un automa sull’alfabeto A. La funzione $\langle\!\langle·\rangle\!\rangle: S → P(A^*)$ è definita per ogni stato $x \in S$ come 
$$\langle\!\langle·\rangle\!\rangle = \{w \in A^* \,|\, \exists y \in F \,|\, (x, y) ∈ T_w \}$$

Il [[Linguaggi formali | linguaggio]] $\langle\!\langle x \rangle\!\rangle$ è detto il **linguaggio accettato** da x. Se $w \in \langle\!\langle x \rangle\!\rangle$, si dice che la [[Stringhe| stringa]] w è accettata dallo stato x (o appartiene al linguaggio accettato da $\mathcal x$). Se $w \notin \langle\!\langle x \rangle\!\rangle$, si dice che la stringa w non è accettata dallo stato x (o non appartiene al linguaggio accettato da $\mathcal x$)

Intuitivamente, per vedere se una stringa w è accettata da uno stato x si devono guardare tutti gli stati y che sono raggiungibili da x con w e, se tra questi c’è almeno uno stato finale, allora la stringa w è accettata, altrimenti non è accettata.

**Automi deterministici e Non**: . Un automa $\mathcal{A}$ = (S, T, F) si dice **deterministico** se la relazione di transizione $T \in Rel(A \times S, S)$ è una funzione. Altrimenti è considerato un **automa non deterministico**.

---
### References

- [[Alfabeto]]
- [[Linguaggi formali]]
- [[Stringhe]]