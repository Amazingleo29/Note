202112101756
Status: #Note
Tags: [[Informatica]] [[Math]] [[FDI]]

# Calcolo Combinatorio

Il **calcolo combinatorio** è la branca della [[Math|matematica]] che studia i modi per raggruppare e/o ordinare secondo date regole gli elementi di un insieme finito di oggetti

### Principio delle buche dei piccioni
Un classico risultato di combinatoria, che ha anche un nome suggestivo, è il cosiddetto Pigeonhole principle o Principio delle buche e dei piccioni. Esso afferma che se abbiamo n piccioni e li vogliamo collocare nelle m caselle di una piccionaia, se n > m allora almeno una casella conterrà due piccioni.
**Definizione**
Dati due [[insiemi]] $P$ e $C$, se $|P| > |C|$ allora non esiste nessuna [[Relazioni|relazione]] $R: P \leftrightarrow C$ che sia [[Proprietà delle relazioni|totale]] e [[Proprietà delle relazioni|iniettiva]]. Infatti se esistesse una tale $R$, e dunque avremmo $|P| \leq |R|$ (R totale) e $|R| \leq |C|$ (R iniettiva), da cui $|P| \leq |C|$ per transitività, contraddicendo l’ipotesi $|P| > |C|$. 

### Regola di [[Biezioni|Biezione]]
Per tutti gli insiemi A, B vale che se esiste una **biiezione** R: A ↔ B, allora |A| = |B|.

### Permutazioni
Le **permutazioni** ci consentono di studiare problemi dove
ci chiediamo, ad esempio, quanti modi diversi ci sono di ordinare un determinato insieme, come appunto il gruppo di amici in pizzeria.
**Definizione**
Dato un insieme finito $A$ con $|A| = n$, una permutazione di $A$ è una sequenza ordinata $a1, ..., an$ dove tutti e soli gli elementi di $A$ appaiono esattamente una volta.

$$P(n) = n!$$ ^fb3b4a

**Anagrammi e permutazioni con ripetizioni**
Esemipo ANNA dovrebbe avre 24 anagrammi possibili secondo la [[#^fb3b4a|formula]], il problema è però che ANNA è composta da sole due lettere distinte, dunque bisogna aggiustare la formula affinche ci dia il numero corretto di anagrammi, e dunque la formula sarà dato $k$ = lunghezza parola e i per ogni lettera che si ripete e in cui $c_k$ per $k \in i$ assume il valore delle volte che la k-esima lettera vine ripetuta all'interno delle parola:

$$P(n)_{con\ ripetizioni} = \frac{k!}{c_0!\cdot c_1!...c_i! } $$

Per Anna:
$$P(4)_{con\ ripetizioni} = \frac{4!}{2!\cdot 2!} = \frac{24}{4} = 6\ anagrammi $$

### Disposizioni
Supponiamo ora che il ristorante non possa mettere tutti gli $n$ amici allo stesso tavolo, ma solamente $k$ di loro, facendo sedere i rimanenti in un’altra sala. In quanti modi diversi possiamo riempire il tavolo con $k$ posti? Chiamiamo questo concetto le disposizioni di $n$ elementi in $k$ posti, note anche come $k$-permutazioni di $n$. ^e15026

**Definizione**
Dato un insieme finito $A$ con $|A| = n$ e un intero $k \leq n$, una disposizione degli elementi di $A$ in $k$ posti è una sequenza ordinata $a_1, ..., a_k$ di elementi di $A$.

$$ D(n) = \frac{n!}{(n-k)!}$$

### Combinazioni

Supponiamo, come all’inizio della [[#^e15026|sottosezione]] precedente, che il ristorante non possa mettere tutti gli $n$ amici allo stesso tavolo, ma solamente $k$ di loro, facendo sedere i rimanenti in un’altra sala. Ci chiediamo ora: in quanti modi diversi possiamo scegliere k degli n amici da far accomodare al tavolo? Chiamiamo questo concetto una combinazione di $k$ elementi di un insieme di cardinalità $n$.

**Definizione**
Sia A un insieme di cardinalità $n$ e sia $k \leq n$ un numero naturale. Una combinazione di $k$ elementi di $A$ è un $k$-insieme di $A$, cioè un sottoinsieme di $A$ di cardinalità $k$. L’insieme di tutte le combinazioni di $k$ elementi di $A$ è quindi denotato con $P_k(A)$.

$$\binom{n}{k} = \frac{n!}{k!(n-k)!} $$

---
### References