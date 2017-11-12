# Aide Mémoire C

Aide mémoire pour le cours de langage C.

## Table des Matières

* [Variables](#variables)  
* [Entrées / Sortie](#entrees_sorties)  
* [Opérateurs](#operateurs)  
* [Structures de Contrôle](#structures_controle)
* [Tableaux](#tableaux)  

<a name="variables"/>

## Variables

``` c
type nom_variable;
``` 

Type | Description 
--- | --- 
int | entier
float | réel
char | caractère

<a name="entrees_sorties"/>

## Entrées / Sorties

### Affichage

``` c
printf("ma valeur=%d",variable);
```

### Lecture

``` c
scanf("%d",&variable);
```

### Indicateurs

Indicateur | Type
--- | ---
%d | int
%f | float
%c | char
%s | char []


<a name="operateurs"/>

## Opérateurs

### Mathématiques

Opérateur | Description | Exemple
--- | --- | ---
+ | Addition | ```resultat=valeur1+valeurs2;```
- | Soustraction | ```resultat=valeur1-valeurs2;```
/ | Division | ```resultat=valeur1/valeurs2;```
% | Modulo (reste de la division entière) | ```resultat=valeur1%valeurs2;```

* Addition: 
* Soustraction: ```resultat=valeur1-valeurs2;```
* Multiplication: ```resultat=valeur1*valeurs2;```
* Division: ```resultat=valeur1/valeurs2;```
* Reste de la division entière (modulo): ```resultat=valeur1%valeurs2;```

### Comparaison

* test d'égalité: ```valeur1==valeurs2;```
* test de différence: ```valeur1!=valeurs2;```

<a name="structures_controle"/>

## Structures de contrôle

### Tests

``` c
if (condition)
{
  //liste d'instructions
}
else
{
  //liste d'instructions
}
```

``` c
switch (variable)
{
  case valeur1: {
    //liste d'instructions
    }
  break;
  case valeur2: {
    //liste d'instructions
    }break;
  default: {
    //liste d'instructions
    }
}
```

### Boucles

``` c
for (indice=0;indice<10;indice++)
{
  //liste d'instructions
}
```

``` c
while(condition)
{
  //liste d'instructions
}
```

``` c
do
{
  //liste d'instructions
}while(condition);
```

<a name="tableaux"/>

## Tableaux

### Declaration / initialisation

``` c
int nom_tableau[nbr_elements]={val_1,val_2,...,val_n};
```

Pour les chaînes de caractères, il est possible d'utiliser la syntaxe

``` c
char nom_tableau[8]="bonjour";   //attention à bien rajouter un element en plus pour stocker le \0
```


### Affectation d'un élèment

``` c
nom_tableau[n] = valeur;
```

### Récuperation d'un élèment

``` c
valeur = nom_tableau[n]; //renvoie la valeur situee a la n+1 "case" du tableau
```
