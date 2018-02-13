# Aide Mémoire C

[![License: CC BY-ND 4.0](https://img.shields.io/badge/License-CC%20BY--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nd/4.0/)


Aide mémoire pour le cours de langage C.

## Table des Matières

* [Variables](#variables)  
* [Entrées / Sortie](#entrees_sorties)  
* [Opérateurs](#operateurs)
  * [Mathématique](#mathematique) 
  * [Comparaison](#comparaison) 
* [Structures de Contrôle](#structures_controle)
  * [if](#if)
  * [switch](#switch)
  * [for](#for)
  * [while](#while)
* [Tableaux](#tableaux)  
* [Structure](#structure)
* [Fonctions](#fonction)

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

Pour utiliser les fonctions d'affichage et de lecture, il faut préalablement ajouter dans l'entête du programme: ```#include <stdio.h> ```

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

<a name="mathematique"/>

### Mathématiques

Opérateur | Description | Exemple
--- | --- | ---
```+``` | Addition | resultat=valeur1+valeurs2;
```-``` | Soustraction | resultat=valeur1-valeurs2;
```/``` | Division | resultat=valeur1/valeurs2;
```%``` | Modulo (reste de la division entière) | resultat=valeur1%valeurs2;

<a name="comparison"/>

### Comparaison

Opérateur | Description | Exemple
--- | --- | ---
```==``` | test d'égalité | valeur1==valeurs2;
```!=``` | test de différence | valeur1!=valeurs2;

<a name="structures_controle"/>

## Structures de contrôle

<a name="if"/>

### if (Test Binaire)

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
<a name="switch"/>

### switch (Test Multiple)

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
<a name="for"/>

### for (Boucle définie)

``` c
for (indice=0;indice<10;indice++)
{
  //liste d'instructions
}
```
<a name="while"/>

### while (Boucle indéfinie)

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

<a name="structure"/>

## Structure

Une structure permet de stocker des informations n'ayant pas forcement le même type.

### Définition (à placer avant le main)

``` c
typedef struct{
     char nom[20];
     char prenom[20];
     int age;
     } personne;
 ```
 
 ### Déclaration (à placer dans le main)
 
 ``` c
 personne etudiant;
 ```
 
 Il est possible d'initialiser les champs en utilisant des accolades
 
  ``` c
 personne etudiant={"Shannon","Claude",50};
 ```
 
 ### Affectation

L'accès à un champs de la structure s'obtient en utilisant le .

``` c
etudiant.age=100;
```

### Récuperation

``` c
annee_naissance=2017-etudiant.age;
```

<a name="fonction"/>

 ## Fonctions
 
 Une fonction correspond à un sous-programme. Il y a globalement deux techniques pour définir une fonction dans le même fichier que le main.
 
 * Technique 1: Déclaration + Définition avant le main
 * Technique 2: Décalaration avant le main, puis définition de la fonction après le main.
 
 La technique 2 est plus modulaire.
 
 ### Déclaration de la fonction (à placer avant le main)
 
 ``` c
 float calcul_module2(float partie_reelle,float partie_imaginaire);
 ```
 
 ### Définition de la fonction (à placer après le main)
 
  ``` c
 float calcul_module2(float partie_reelle,float partie_imaginaire)
 {
    float module2;
    
    module2=partie_reelle*partie_reelle+partie_imaginaire*partie_imaginaire;
 
    return module2;
 }
 ```
  
 ### Appel d'une fonction (à placer dans le main ou dans une autre fonction)

  ``` c
  module2=calcul_module2(1,3);
   ```
  
