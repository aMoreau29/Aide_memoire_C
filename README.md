# Aide_memoire_C
Groupe TP12A

## Variables

``` c
type nom_variable;
``` 

Types possibles:
* int (entier)
* float (réel)
* char (caractère)

## Entrées / Sorties

### Affichage

``` c
printf("ma valeur=%d",variable);
```

Indicateur en fonction du type de variable
* %d: int
* %f: float
* %c: char
* %s: char []

### Lecture

``` c
scanf("%d",&variable);
```
## Opérateurs

### Mathématiques

* Addition: ```resultat=valeur1+valeurs2;```
* Soustraction: ```resultat=valeur1-valeurs2;```
* Multiplication: ```resultat=valeur1*valeurs2;```
* Division: ```resultat=valeur1/valeurs2;```
* Reste de la division entière (modulo): ```resultat=valeur1%valeurs2;```

### de Comparaison

* test d'égalité: ```valeur1==valeurs2;```
* test de différence: ```valeur1!=valeurs2;```

## Structure de contrôle

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



## Tableaux

### Declaration / initialisation

``` c
int nom_tableau [nbr_elements]={val_1,val_2,...,val_n};
```

### Affectation d'une valeur d'un tableau

``` c
nom_tableau[n] = valeur;
```

### Récuperation d'un élèment du tableau

``` c
valeur = nom_tableau[n]; //renvoie la valeur situee a la n+1 "case" du tableau
```
