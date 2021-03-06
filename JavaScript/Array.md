# Javascript 

## Description

Les tableaux sont des objets qui possèdent des méthodes incorporées, ni la taille du tableau ni les éléments n'est fixe, puisque nous pouvons ajouter ou enlever des éléments dedans. Il faut savoir que le premier élément d'un tableau est TOUJOURS l'index 0 ! 

Voici les syntaxes :

```js
const arr = ["Elem1", "Elem2", "Elem3"]
const secondArray = new Array("elem1", "elem2", "elem3")
```

Les 2 syntaxes vont afficher la même chose, mais la première est la plus utilisée.

## connaître le nombre d'éléments dans un tableau

Pour connaître le nombre d'éléments dans un tableau c'est assez facile il suffit d'utiliser la propriété `.length` 

```js
const Myarr = ["apple", "bananas", "orange", "lemon"]
console.log(Myarr.length)
```

On peut donc voir dans la console : `4`, c'est le nombre d'éléments total qu'il y a dans le tableau.

## Trouver un élément dans un tableau à partir d'un index

Pour trouver un élément dans un tableau à partir d'un index il va falloir utiliser `array[x]`, x représentant l'index. (ATTENTION il ne faut pas oublier
qu'un tableau commence toujours par l'index 0).

```js
const findElem = ["index0", "index1", "index2","index3"]
console.log(findElem[1])
```

dans la console `index1` va donc être affiché.

## Trouver le dernier élément dans un tableau

La propriété `length-1` va nous donner le dernier élément d'un tableau.

```js
const last = [3, 8, 238, 278]
console.log(last[last.length-1]) // Affiche 278
```

## Ajouter un élément au début du tableau

La méthode `unshift()` va nous permettre d'ajouter un ou plusieurs éléments au début du tableau.

```js
const addStart = [2, 923, 2093]
addStart.unshift(300)
console.log(addStart) // Affiche [300, 2, 923, 2093]
```

## Ajouter un élément à la fin du tableau

Pour ajouter un élément à la fin du tableau il faut utiliser la méthode `push()`

```js
const addEnd = [2, 923, 2093]
addEnd.push("apple")
console.log(addEnd) // Affiche [2, 923, 2093, "apple"]
```

## Supprimer un élément au début du tableau

Il faut utiliser la méthode `shift()` pour supprimer un élément au début du tableau

```js
const deleteStart = ["delete", "not delete"]
deleteStart.shift()
console.log(deleteStart) // Affiche ["not delete"]
```

## Supprimer un élément à la fin du tableau

Pour supprimer un élément à la fin du tableau il faut utiliser la méthode `pop()`

```js
const deleteEnd = ["i am still here", "i am delete"]
deleteEnd.pop()
console.log(deleteEnd) // Affiche ["i am still here"]
```

## Trouver l'index d'un élément dans un tableau

Pour trouver l'index d'un élément dans un tableau, il va falloir utiliser la méthode `indexOf()`, il est sensible à la casse il faut donc faire attention de bien mettre la majuscule.

```js
const findIndex = [7687, 0876, 23, 021]
console.log(findIndex.indexOf(23)) // Affiche 2
```

Par contre si l'élément renseigné n'est pas trouvé dans le tableau, `-1` sera affiché

```js
const findIndexFalse = [7687, 0876, 23, 021]
console.log(findIndexFalse.indexOf(25)) // Affiche -1
```

## Trouver l'index du dernier élément que l'on recherche dans le tableau

Par exemple si dans un tableau il y a plusieurs fois la même information mais que nous voulons juste le dernier nous pouvons utiliser `lastIndexOf()` pour trouver son index 

```js
const findLastIndex = [1, 2, 12, 192, 11,234, 901, 11]
console.log(findLastIndex.lastIndexOf(11)) // Affiche 7
```

tout comme `indexOf()`, si l'élément renseigné n'est pas trouvé dans le tableau, `-1` sera affiché

## Supprimer un ou plusieurs élément grâce à leurs index

Pour supprimer un ou plusieurs élément dans un tableau, il faut utiliser la méthide `splice()`

```js
const deleteElem = ["Apple", "Orange", "Bananas", 123]
deleteElem.splice(2,2)
console.log(deleteElem) // Affiche ["Apple", "Orange"]
```

Comme nous pouvons le voir dans l'exemple au-dessus, la méthode `splice()` prend 2 paramètres le 1er c'est l'index et le deuxième c'est le nombre d'éléments à supprimer

## Exploser une chaîne de caractères en tableau

Pour exploser une chaîne de caractères en tableau il faut utiliser la méthode `split()`

```js
const str = "Facebook/Twitter/Instagram/Linkedin"
const table = str.split("/")
console.log(table) // Affiche ["Facebook" "Twitter" "Instagram" "Linkedin"]
```

Le `("/")` permet de supprimer le slash entre chaque mot.

## Transformer un tableau en chaîne de caractères

Maintenant que nous avons vu comment avoir un tableau à partir d'une chaîne de caractères, nous allons voir comment faire l'inverse, c'est-à-dire transformer un tableau en chaîne de caractères, pour ce faire il va falloir utiliser la méthode `join()`

```js
const ArrayJoin = ["Apple", "Bananas", "Orange"]
console.log(ArrayJoin.join(", ")) // Affiche "Apple, Bananas, Orange"
```

Le `(", ")` va mettre une virgule ET un espace entre chaque mot.

## Copier un tableau

Pour copier un tableau, il faut utiliser la méthode `slice()`

```js
const copyArray = ["Name", "Surname", "Username"]
console.log(copyArray.slice()) // Affiche ["Name", "Surname", "Username"]
```

il est aussi possible de copier qu'une partie du tableau

```js
const secondCopy = ["Name", "Surname", "Username"]
console.log(secondCopy.slice(1,3))
```

le 1er paramètre (1) correspond à l'index du début du tableau que l'on va copier, le 2ieme paramètre (3) correspond à la fin du tableau que l'on va coper

## Retourner un tableau

Pour retourner un tableau il faut utiliser la méthode `reverse()`

```js
const arrayReverse = [1,2,3,4,5]
console.log(arrayReverse.reverse()) // Affiche [5,4,3,2,1]
```

## Trier un tableau par ordre croissant

Pour trier un tableau par ordre croissant ou par ordre alphabétique, il va falloir utiliser la méthode `sort()`

```js
const arraySort = ["Zorro", "Hercule", "Ulysse"]
console.log(arraySort.sort()) // Affiche ["Hercule", "Ulysse", "Zorro"]
```

```js
const arraySort = ["Zorro", "Hercule", "Ulysse"]
console.log(arraySort.sort()) // Affiche ["Hercule", "Ulysse", "Zorro"]
```

## Trier un tableau par ordre décroissant

Pour trier un tableau par ordre décroissant, nous allons avoir besoin de 2 méthodes que nous avons déjà vues ici, la méthode `reverse()` et la méthode `sort()`

```js
const reverseSort = ["Zorro", "Hercule", "Ulysse"]
console.log(reverseSort.reverse(reverseSort.sort())) // Affiche ["Zorro", "Ulysse", "Hercule"]
```

```js
const reverseNumber = [5, 2, 1, 9]
console.log(reverseNumber.reverse(reverseNumber.sort())) // Affiche [9,5,2,1]
```

## Fusionner 2 tableaux

Pour fusionner 2 tableaux (ou plus), il va falloir utiliser la méthode `concat()`

```js
const arrayConcat = ["This", "is a test"]
const anotherArrayConcat = ["for", "concat"]
console.log(arrayConcat.concat(anotherArrayConcat)) // Affiche ["this", "is a test", "for", "concat"]
```

## Filtrer des éléments dans un tableau

Pour filtrer des éléments dans un tableau on va devoir utiliser `filter()`

```js
const age = [15, 22, 11, 95]
function checkAdult(age){
    return age >= 18
}
console.log(age.filter(checkAdult)) // Affiche [22, 95]
```

`filter` va retourner un nouveau tableau avec tous les éléments qui ont passé le test.

## Vérifier si une valeur est présente dans le tableau

Pour vérifier si une valeur est présente dans le tableau il faut utiliser la méthode `include()` et mettre l'élément que l'on recherche en argument, Retourne `true` si l'élément est trouvé dans le tableau, sinon retourne `false`

```js
const numVerif = [22, 11, 18, 16, 14, 12]
console.log(numVerif.includes(22)) // Affiche true
console.log(numVerif.includes(2)) // Affiche false 

const stringVerif = ["Lamb", "Goose", "Deer"]
console.log(stringVerif.includes("Lamb")) // Affiche true
console.log(stringVerif.includes("Lambe")) // Affiche false
```

## Réduire une liste de nombre à une seule valeur

Pour réduire une liste de nombre à une seule valeur, il va falloir utiliser la méthode `reduce` cette méthode applique une fonction, un `accumulateur` qui traite chaque valeur d'une liste (de la gauche vers la droite) afin de la réduire en une seule valeur.

Voici la syntaxe : 
```js
arr.reduce(callback, valeurInitiale)
```

et voici un exemple :

```js
let arr = [1, 2, 3, 4, 5];
let sum = arr.reduce((a, b) => a + b);
console.log(sum);
```

Pour cet exemple la fonction `callback` va être appelée 4 fois :

*   Le premier appel : `l'accumulateur` va être de 1 et la `valeur courante` de 2, la `valeur retournée` sera : 3
*   Le deuxième appel : `l'accumulateur` va être de 3 et la `valeur courante` de 3, la `valeur retournée` sera : 6
*   Le troisième appel : `l'accumulateur` va être de 6 et la `valeur courante` de 4, la `valeur retournée` sera : 10
*   Le quatrième appel : `l'accumulateur` va être de 10 et la `valeur courante` de 5, la `valeur retournée` sera : 15

La valeur retournée va donc être celle du dernier appel, pour l'exemple ci-dessus ce sera donc 15.

## Boucler dans un tableau

Description : boucler dans un tableau est un moyen pour répéter une / ou des actions rapidement et facilement. il existe différents types de boucle, chaque type peut être utilisé en fonction de la situation du problème que l'on a.

Voici les différents types de boucle :

### la boucle for
```js
const firstLoop = ["elem1","elem2", "elem3"]
for(let i = 0; i <firstLoop.length; i++){
    console.log(firstLoop[i]) // Affiche "elem1", "elem2", "elem3"
}
```

### La boucle for... of
```js
const secondLoop = ["elem1","elem2", "elem3"]
for(let elem of secondLoop){
    console.log(elem) // Affiche "elem1", "elem2", "elem3"
}
```

### La boucle for... in 

```js
const thirdLoop = ["elem1","elem2", "elem3"]
for(let third in thirdLoop){
    console.log(thirdLoop[third]) // Affiche "elem1", "elem2", "elem3"
}
```