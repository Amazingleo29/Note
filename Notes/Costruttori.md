202112011702
Status: #Note
Tags: [[Informatica]] [[Laboratorio]]

# Costruttori
**Quando si usano?**: Si usano quando si a che fare oggetti complicati, è usuale (e comodo) usare una funzione per costruire l’oggetto, spesso partendo da alcuni valori che lo descrivono.

Queste funzioni usano il fatto - che già conosciamo - che ogni volta che viene valutato un **letterale di tipo oggetto**$^1$ in effetti viene allocato un nuovo oggetto, con un suo riferimento diverso da tutti quelli già esistenti.

Spesso queste funzioni prevedono argomenti di default, oppure effettuano dei calcoli o dei controlli prima di inizializzare l’oggetto.

**this**$^2$: fa riferimento all'oggetto che chiama il metodo

**new**$^3$:  genera nuovo oggetto vuoto, chiama il costruttore passando this più eventuali parametri, il risultato è l'oggetto inizializzato

```js
//Nota 1
var persona = {
	cognome: gervasi,
	età: 10
}

//Nota 2

persona.compleanno = () => {this.età++}
/* crea la funzione compleanno e la
assegna all'oggetto persona */

vincenzo.compleanno() //aumenta di 1 l'età di vincenzo

//Nota 3

function CostruisciPersone(n, c, e){
	this.nome = n,
	this.cognome = c,
	this.età = e
}

var gerva = new CostruisciPersona("Vincenzo",  "Gervasi", "50"/*?*/)

```

---
### References