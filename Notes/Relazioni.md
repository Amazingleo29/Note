202112071640
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Relazioni

**Definizione**
Una **relazione** $R$ tra l’[[Insiemi|insieme]] $A$ e l’insieme $B$ è un sottoinsieme del prodotto cartesiano $A \times B$, quindi $R \subseteq A \times B$. Indicheremo l’insieme di tutte le relazioni tra $A$ e $B$ con la notazione $Rel(A, B)$. Per indicare che $R$ è una relazione tra $A$ e $B$, cioè $R \in Rel(A, B)$, scriveremo spesso $R: A \leftrightarrow B$.

**Osservazione**: Si noti che dalla definizione segue che $Rel(A, B) = P(A \times B)$. Data una relazione $R: A \leftrightarrow B$ e due elementi $a \in A$ e $b \in B$, se $(a, b) \in R$ diremo che $a$ è in relazione $R$ con $b$.

---

### Operazioni sulle relazioni

Data una relazione $R: A \leftrightarrow B$.
Le relazioni possono essere viste come insiemi di coppie $(a,b)$ in cui $a \in A$ e $b \in B$, dunque essendo [[insiemi]] si possono applicalre le stesse operazioni con le dovute precauzioni, cioè per le due relazioni devono essere relazioni sugli stessi inisemi.

**Composizione**
- È un’operazione che permette di combinare due relazioni, quando l’insieme di arrivo della prima relazione è lo stesso dell’insieme di partenza della seconda.

- **Definizione**
Siano $R: A \leftrightarrow B$ e $S: B \leftrightarrow C$. La composizione di $R$ con $S$ è la relazione $R; S : A \leftrightarrow C$ così definita
$$R;S = \{(x,z) \in A \times C \;|\; \exists \; y\in B\;.(x,y)\in R \land (y,z) \in S\}$$

**Relazione opposta**
Sia $R: A \leftrightarrow B$ una relazione. La relazione opposta di $R$ è la relazione $R^{op}: B \leftrightarrow A$ definita come
$$R^{op} = \{(y,x) \in B\times A \;|\; (x,y) \in R\}$$

---
### Leggi
[[Cheat Sheet - Insiemi Relazioni e Logica.pdf|Leggi sulle relazioni]]

---

### Proprietà delle relazioni
[[Proprietà delle relazioni]]

---
### References
- [[Insiemi]]