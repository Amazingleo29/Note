202112110912
Status: #Note
Tags: [[Informatica]] [[FDI]]

# Induzione strutturale e ricorsione

**Segnatura**
Una **segnatura** è una famiglia di [[insiemi]] indicizzata da $N$, cioè $\mathcal{F} = \{\mathcal{F}_n\}_{n\in N}$ . Gli elementi di tale famiglia sono detti **simboli**. Per ogni $n \in N$, $\mathcal{F}_n$ è l’insieme dei simboli di arietà $n$ (o con $n$ argomenti). I simboli di arietà $0$ sono detti **simboli di costante**.

**Termini**
Data una segnatura $\mathcal{F}$, l’insieme $\mathcal{F}Term$ degli $\mathcal{F}$-termini è il più piccolo insieme che soddisfa:

1. per ogni simbolo $c\in \mathcal{F}_0, c \in \mathcal{F}Term$;
2. per ogni $n \geq 1$ ed ogni simbolo $f \in \mathcal{F}_n$, se $t_1, ...,t_n \in \mathcal{F}Term$ allora $f(t_1, ...,t_n) \in \mathcal{F}Term$

## Principio di induzione strutturale

È possibile formulare il **Principio di Induzione** a livello degli $\mathcal{F}$-termini e i principi per naturali, [[liste]] e alberi possono essere ricavati come casi speciali di questo, opportunamente fissando la segnatura $\mathcal{F}$. Il Principio di Induzione sui termini viene comunemente chiamato ***Principio di Induzione Strutturale***. Il Principio di Induzione Strutturale stabilisce che:

1. se (caso base), per ogni simbolo $c ∈ \mathcal{F}_0$, $P(c)$ è vera, e
2. se (caso induttivo), per ogni $n \geq 1$, per ogni simbolo $f \in \mathcal{F}_n$, per tutti i termini $t_1, ..., t_n \in \mathcal{F}Term$, vale che se $P(t_1), ..., P(t_n)$ sono vere allora anche $P(f(t1, ..., tn)$) è vera,

allora $P(t)$ è vera per ogni $t \in \mathcal{F}Term$ 
In modo più compatto possiamo scrivere il **Principio di Induzione Strutturale** come una **regola di inferenza**:
$$\frac{∀c ∈ F0 . P(c)\ \ ∀n ≥ 1 . ∀f ∈ Fn . ∀t1, . . . , tn ∈ FT erm . P(t1) ∧ · · · ∧ P(tn) ⇒ P(f(t1, . . . , tn))}{∀t ∈ FTerm . P(t)}$$


## Ricorsione

Le [[funzioni]] definite induttivamente sono un caso particolare di **funzioni ricorsive**. Una funzione è detta **ricorsiva** se il valore della funzione per un certo argomento è **espresso in termini del valore della stessa funzione applicata a uno o più argomenti**, non necessariamente più piccoli

**Relazione di precedenza indotta da una definizione ricorsiva**
Data una definizione ricorsiva di $rec : A \rightarrow B$, la [[Relazioni|relazione]] di precedenza indotta è la relazione $\prec_{rec} \in Rel(A, A)$ definita come segue:
$$per\ ogni\ x, y ∈ A,\ x \prec_{rec}\ y\ se\ e\ solo\ se\ rec(y) $$$$è\ definita\ direttamente\ in\ termini\ di\ rec(x)$$

**Relazione ben fondata**
Una relazione $\sqsubset$ su un insieme $A$, $\sqsubset \in Rel(A, A)$, è ben fondata se non esiste una catena infinita decrescente ^400cbf

$$ a_1 \sqsupset a_2 \sqsupset a_3 \sqsupset a_4 \sqsupset\ ...$$

di elementi $a_i \in A$

**Ben data**
Data una definizione ricorsiva di $rec : A \rightarrow B$, essa è **ben data** (e quindi $R_{rec}$ è [[Proprietà delle relazioni|univalente]] e [[Proprietà delle relazioni|totale]]) se 
1. per ogni elemento $a \in A$ c’è esattamente una clausola della definizione applicabile per valutare $rec(a)$ e,
2. la relazione $\prec_{rec}$ è [[#^400cbf|ben fondata]].

### Tipologie di ricorsione
**Ricorsione annidata**
Si ha **ricorsione annidata** quando una funzione compare come parametro in una sua chiamata ricorsiva.

**Ricorsione mutua**
Quando la chiamata ricorsiva avviene indirettamente, cioè da parte di una seconda funzione chiamata a sua volta, direttamente o indirettamente, dalla prima, si parla di ricorsione *mutua* o *indiretta*

**Ricorsione procedurale**
In questo capitolo abbiamo discusso della definizione di funzioni ricorsive, intendendo funzioni nel senso matematico del termine. Ma quando si deve risolvere un problema con un programma, nella maggior parte dei linguaggi di programmazione si possono usare anche effetti collaterali (come input e output, o modifica di variabili/array con assegnamento) che non sono rappresentabili immediatamente come funzioni matematiche. In molti linguaggi una procedura può essere invocata passando degli argomenti, ma non ci si aspetta che restituisca un risultato. Un tipico esempio sono le funzioni in C/C++ o i metodi in Java che sono dichiarati di tipo void. Anche le procedure naturalmente possono essere ricorsive, terminando quando l’input è “abbastanza piccolo” (tipicamente senza fare niente), o altrimenti invocando se stesse su argomenti “più piccoli”.

---
### References