# Javascript

## Les variables 

Une variable est un "stockage nommé" pour les données. Nous pouvons utiliser des variables pour stocker des goodies, des visiteurs et
d'autres données.

Pour créer une variable en Javascript, nous devons utiliser le mot `let`.

L'instruction ci-dessous déclare une variable avec le nom "message".
```js
let message;
```

Maintenant nous pouvons y mettre des données en utilisant l'opérateur d'affection `=`
```js
let message;
message = "Hello";
```

La chaîne de caractères est maintenant associée à la variable, nous pouvons y accéder en utilisant le nom de la variable :
```js
let message;
message = "Hello";
alert(message); //afficher le contenu de le variable
```

Nous pouvons déclarer la variable sur une seule ligne : 
```js
let message = "Hello";
```

Nous pouvons aussi déclarer plusieurs variables sur la même ligne : 
```js
let user = "Gérard", age = "21", message = "Hello";
```

ça peut sembler plus court, mais ce n'est pas recommandé, pour une meilleure visibilité il faut utiliser 1 ligne par variable.
La variable multiligne est un peu plus longue mais est plus facile à lire : 
```js
let user = "Gérard";
let age = "21";
let message = "Hello";
```

le mot-clé `var` est presque identique à `let`. Il déclare également une variable, mais d'une manière légèrement différente, en mode "old school".