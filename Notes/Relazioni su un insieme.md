202112091608
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Relazioni su un insieme

**Definizione**
Una [[Relazioni|relazione]] $R$ sull'[[Insiemi|insieme]] $A$ è un sottoinsieme del prodotto cartesiano $A \times A$, quindi $R \subseteq A \times A$. Indicheremo l'insieme di tutte le relazioni su $A$ con la notazione $Rel(A,A)$, e una relazione $R \in Rel(A,A)$ come $R: A \leftrightarrow A$.

### Proprietà di relazioni su un insieme

**Riflessiva**
Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è **riflessiva** se per tutti gli elementi di $a \in A$ vale che 
$$(a,a) \in R$$

**Transitiva**
Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è **transitiva** se per tutti gli elementi $a,b,c, \in A$, vale che
$$ se\;(a,b) \in R \;\;e\;\; (b,c) \in R,\;allora\;\;(a,c) \in R$$

**Simmetrica**
Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è **simmetrica** se per tutti gli elementi $a,b \in A$, vale che 
$$ se\;(a,b) \in R,\;allora\;\;(b,a) \in R$$

**Anti-simmetrica**
Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è **anti-simmetrica** se per tutti gli elementi $a,b \in A$, vale che 
$$ se\;(a,b) \in R \;\;e\;\; (b,a) \in R,\;allora\;\; a = b$$

### Teorema di caratterizzazione

Le relazioni riflessive, transitive, simmetriche e anti-simmetriche possono essere caratterizzate attraverso le operazioni su relazioni

- $R$ è **riflessiva** se e solo se $id_A \subseteq R$;
- $R$ è **transitiva** se e solo se $R;R \subseteq R$;
- $R$ è **simmetrica** se e solo se $R^{op} \subseteq R$;
- $R$ è **anti-simmetrica** se e solo se $R \cap R^{op} \subseteq R$;

### Chiusure

Data una relazione $R: A \leftrightarrow A$ è sempre possibile trasformarla in una relazione riflessiva seguendo una ricetta standard.

**Chusura riflessiva**
Sia $R: A \leftrightarrow A$ una relazione su $A$. La **chiusura riflessiva** di $R$ è la relazione $R \cup id_A$.

**Chiusura simmetrica**
Sia $R: A \leftrightarrow A$ una relazione su $A$. La **chiusura simmetrica** di $R$ è la relazione $R \cup R^{op}$

**Chiusura transitiva**
Sia $R: A \leftrightarrow A$ una relazione su $A$. La **chiusura transitiva** di $R$, denotata $R^+$, è la relazione definita come
$$R^+ = \bigcup_{n\ \in\ \mathbb{N}^+} R^n$$
l'idea è di applicare la chiusura un numero di volte tale per cui R;R = R

**Stella di Kleene**
Sia $R: A \leftrightarrow A$ una relazione su $A$. La chiusura **transitiva e riflessiva** di $R$, denotata $R^+$, è la relazione definita come
$$R^* = \bigcup_{n\ \in\ \mathbb{N}} R^n$$
 
### Relazioni di Equivalenza

Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è una **relazione di equivalenza** se è riflessiva, transitiva e simmetrica.

### Relazioni di ordinamento
**Ordinamento parziale**
Sia $R: A \leftrightarrow A$ una relazione su $A$. Si dice che $R$ è una **relazione di ordinamento parziale** se è riflessiva, transitiva ed anti-simmetrica

Esempio : $\leq$ è una relazione di ordinamento parziale

**Ordinamento**
Sia $R: A \leftrightarrow A$ una relazione di ordinamento parziale su $A$. Si dice che $R$ è un **ordinamento** se
$$per\ tutti\ gli\ (a,b) \in A \times A, vale\ che\ (a,b) \in R\ oppure\ (b,a) \in R$$

---
### References
- [[Insiemi]]
- [[Relazioni]]
