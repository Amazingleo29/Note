202112041512
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Grammatiche libere da contesto
**Definizione** 
Una **grammatica libera da contesto** $\mathcal{G}$ sull’alfabeto A consiste di una coppia (S, P) dove:
- S è l'nsieme dei simboli non terminali (S è disgiunto da A)
- P è un insieme di produzioni: ogni produzione ha la forma $$\langle X \rangle ::= w$$ dove $\langle X \rangle \in S$ e $w \in (A \cup S)^*$ si noti che w può essere la stringa vuota $\varepsilon$.

Una grammatica $\mathcal{G}$ si dice finita se l'insime dei terminali S è finito.

**Per cosa si usano?**
Un’importante applicazione delle grammatiche è la specifica della sintassi dei linguaggi di programmazione: le grammatiche costituiscono, infatti, una notazione comoda e concisa per descrivere la sintassi di un tipico linguaggio di programmazione.

**Albero di derivazione sintattica**
Sia (S, P) una grammatica libera da contesto sull’alfabeto A. Un albero di derivazione sintattica (o parse tree) è un albero radicato dove:
- ogni nodo interno è etichettato da un simbolo non terminale (cioè un simbolo in S)
- ogni foglia è etichettata da un simbolo terminale (cioè un simbolo in A) o la stringa vuota 
- ogni nodo interno v rappresenta l’applicazione di una produzione, ovvero deve esistere una produzione tale che:
	-  (a) l’etichetta del nodo v è la testa della produzione 
	-  (b) l’etichette dei figli di v, da sinistra a destra, formano il corpo della produzione.

Sia $w \in A^*$ la stringa ottenuta leggendo da sinistra a destra i simboli terminali che etichettano le foglie dell’albero (la stringa vuota si ignora). Si dice w è la stringa testimoniata dall’albero o che l’albero è un albero di derivazione (sintattica) di w.

---
### References
- [[Alfabeto]] espressioni aritmetiche $A = \{+, −, ×, ÷\} \cup \{0, 1, 2,..., 9\} \cup \{a, b, c,..., z\}$
- Si usa la notazione BNF