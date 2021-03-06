# Typescript
## Cette partie du cheat-sheets est en cours de développement

## Introduction

## Installation de Typescript

Pour installer Typescript il faut faire : 
```bash
npm install -g Typescript
```

Cette installation donne accès à la commande `tsc`, La commande permettra de Transpiler le code en JavaScript (ES3, ES5 ou ES2015)
```Typescript
tsc index.ts
```

## Les variables dans Typescript

Le principal atout de Typescript c'est d'associer facultativement un type à une donnée.
```Typescript
let pi: number;
let message: string;
let flag: boolean;
let joker: any;
```
Dans l'exemple ci-dessus quatre variables sont déclarées sans être initialisées.

*   La variable pi a pour type : number c'est un nombre entier ou flottant

*   La variable message a pour type : string c'est une chaine de caractères

*   La variable flag a pour type : boolean il peut prendre true or false

*   La variable joker a pour type any : c'est le type par défaut que Typescript attribue pour une variable globale si il ne parviens pas à
déterminer son type lors de la déclaration

il est tout à fait possible d'initialiser une variable quand on la déclare : 
```Typescript
let pi = 3.14;
let message = "Hi";
let flag = true;
let joker = null;  
```
Lors de la première initialisation Typescript en infère automatiquement le type sans qu'il soit nécessaire de le mentionner.

Ainsi, Typescript, contrairement à JavaScript, peut être considéré comme un langage à typage statique.

définition par MDN d'un typage statique : 

Un langage à typage statique est un langage (comme Java, C ou C++) avec lequel les types des variables sont connus lors de la compilation et doivent être spécifiés expressément par le programmeur.

## Fonction 

Le langage Typescript permet de préciser le type du résultat attendu lors de la déclaration de la fonction.

Par défaut, et sans l'instruction return, le type de résultat d'une fonction est `void` (aucun résultat).
```Typescript
function double(n:number) :number{
    return 2 * n;
}
```

La fonction double ci-dessus prend est déclarée comme prenant un paramètre de type number et renvoie une valeur de type number.

## Classe 

```Typescript
class Animal {
    name: string;

    constructor(name: string) {
        this.name = name;
    }
    shout(): string{
        return"...";
    }
}
```
comme ont peut le voir ci-dessus une classe Animal y est définis d'une façon proche de la plupart des langages orientés objet.

La classe Animal possède un attribut `name` elle définit un `constructor` et une méthode `shout` son instanciation se fait à l'aide de 
l'opérateur new : 
```Typescript
var animal = new Animal("Pokemon");
```

Typescript implémente aussi la notion d'héritage simple avec l'utilisation du mot-clés `extends`

L'extension de la classe Animal de l'exemple précédent se fait ainsi : 
```Typescript
class Lion extends Animal{
    sex: string;
    
constructor(name : string, sex: string){
    super(name);
}
shout(): string {
    return "Rooooaaaarrr"
}
}
```

La classe Lion ajoute un attribut sex à la class Animal et redéfinit la méthode SHOUT.

dans Typescript toutes les classes sont considérées comme de nouveaux types, donc pour l'exemple ci-dessus 
la classe Lion est de type Lion et avec l'héritage elle est aussi du type Animal 