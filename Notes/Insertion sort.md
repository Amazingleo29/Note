202111292227
Status: #Note
Tags: [[Informatica]] [[ProgAlg]] [[Sorting algorithm]]

# Insertion sort

**Idea**: Immagina di avere delle carte in mano per semplicità tutte dello stesso seme e di doverle ordinare in maniera crescente da sinistra a destra, dunque inizi dalla seconda carta e guardi se è in ordine ripetto alla prima, se lo è le lasci così sennò le scambi, poi ripeti la stessa cosa per la terza e quindi guardi se è in ordine con la seconda, se lo è la lasci li altrimenti la scambi con la seconda, se l'hai scambiata con la seconda controlla dunque che sia in ordine anche con la prima, se è cosi la lasci li altrimenti la scambi con la prima... e continui così finche non hai ordinato tutte le carte

Complessità:
- Caso ottimo: $\Theta(n^2)$

```js
function insertionSort(a){
  for (var i = 1; i < a.length; i++){
		while (a[i-1] > a[i] && i > 0){
			[ a[i-1], a[i] ] = [ a[i], a[i-1] ]
			i--
		}
	}
}
```

---
### References