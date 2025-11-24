#TP1 
### Nom: Ajlali
### Prenom:Marwa 

## EXERCICE 1 : 
```
ALGORITHME: Code_Pin 
 VAR  contour :constante 
             PIN : entier 
             pi    : 3235 
 DEBUT 
        contour  <-- 0 
        Repeter 
                écrire ("Donnez le code PIN ") 
                 lire ("Pin")
         contour <-- c+1 
        Si ( PIN= pi ) alors 
                 écrire ("le code est vérifiée avec succès") 
        Sinon 
        Si (PIN≠pi ) alors 
                 écrire ("erreur") 
         Sinon 
        Si (PIN!=pi ou c=3) alors
                  écrire ("blocage")
        Finsi 
    Finsi 
 Finsi
FIN
```
## EXERCICE 2 : 
```
ALGORITHME:échange_des_variavles
VAR    x,y,z : entier 
 
DEBUT 
         écrire ("donnez deux variables ") 
          lire("x,y") 
          z <-- y
          y <-- x 
          x <-- z 
          écrire ("y"="y" ,"x"="x")
  FIN
```
## EXERCICE 3 : 
 # q1 
```
ALGORITHME : PGCD 
  VAR     PGCD ,a,b :entier 
 
DEBUT 
         écrire ("donnez deux nombres ")
         lire (a,b )
        Tant que b!= faire 
          r <-- a mod b
          a <-- b 
          b <-- r 
     Fin tanque 
        écrire ("le PGCD est : "a" " ) 
FIN
 la complexite est : O(log(min(a, b)))
```
 # q2 : 
```

ALGORITHME pgcd_recursif
 VAR a, b, resultat : Entier

Fonction pgcd(x : Entier, y : Entier) : Entier
    Si (y = 0) Alors
        retourne x
    Sinon
        retourne pgcd(y, x mod y)
    Finsi
Fin Fonction

DEBUT
    ecrire("Donner a : ")
    lire(a)
    ecrire("Donner b : ")
    lire(b)
    resultat <-- pgcd(a, b)
    ecrire("PGCD = ", resultat)
Fin
 la complexité est : O(log(min(a, b)))
```
###  EXERCICE 4 : 
# Q1 méthode 1 :  
```
 ALGORITHME Diviseurs_méthode1
VAR   n, b : entier

Début
    écrire ("Donner un nombre : ")
    Lire( n )
    Pour b allant de 1 à n faire
        Si n mod b = 0 alors
            Rettourne b
        Fin Si
    Fin Pour
Fin
 La complexité est : O(n)
```
# Q2 :méthode 2   
```
Algorithme Diviseurs2
VAR   n, d : entier

Début
     écrire ("Donner un nombre : ") 
    Lire (n)
    Pour d allant de 1 à racineCarree(n) faire
        Si n mod d = 0 alors
            Rettourne d
            Si d != n / d alors
                Rettourne  n / d
            Fin Si
        Fin Si
    Fin Pour
Fin
  La complexité est : O(√n)
```
### EXERCICE 5: 
```
ALGORITHME deviner_nombre
VAR n, x, tentative : entier
    rejouer : chaine

DÉBUT 
    rejouer <-- "oui"

    tant que (rejouer = "oui") faire

        n <-- aleatoire(1, 100)
        tentative <-- 0

        tant que (tentative < 5) faire
         ecrire("devinez un nombre entre 1 et 100 : ")
            lire(x)
            tentative <-- tentative + 1

            SI (x = n) alors
            ecrire("félicitations ! vous avez trouvé le nombre.")
            SINON
                si (x > n) alors
                    ecrire("trop grand")
                SIMON 
                    ecrire("trop petit")
                FIN SI 
            FIN SI 
      FIN TANT que
                Si (x != n) alors
         ecrire("vous avez perdu. le nombre correct était : ", n)
        FIN SI 

        ecrire("voulez-vous rejouer ? (oui/non)")
        lire(rejouer)

    fin tant que

FIN 
 ```
### EXERCICE 6 : 
```
ALGORITHME triangle_floyd
Var n : entier

Procedure afficher_floyd(lignes : entier)
Var i, j, k : entier
DEBUT
    k <-- 1
    Pour i <-- 1 JusquA lignes Faire
        Pour j <-- 1 JusquA i Faire
            ecrire(k, " ")
            k <-- k + 1
        FinPour
        ecrire("")   // retour à la ligne
    FinPour
FIN

DEBUT
    ecrire("donner le nombre de lignes : ")
    lire(n)
    écrire _floyd(n)
FIN
  La complexité de l’algorithme est :  O(n²)
car on écrit 1 + 2 + ... + n = n(n+1)/2 nombres.
```
### EXERCICE 7 : 
## Q1 :
``` 
ALGORITHME somme_entiers
Var n, i, somme : entier
DEBUT
    somme <-- 0
    ecrire("donner un nombre n : ")
    lire(n)
    
    Pour i <-- 1 JusquA n Faire
        somme <-- somme + i
    FinPour

    ecrire("la somme des entiers de 1 a ", n, " est : ", somme)
FIN
```
## Q2 : 
```
ALGORITHME somme_entiers_recursif
Var n, resultat : entier

Fonction somme(n : entier) : entier
DEBUT
    Si n = 0 Alors
        retourne 0
    Sinon
        retourne somme(n-1) + n
    FinSi
FIN

DEBUT
    ecrire("donner un nombre n : ")
    lire(n)
    resultat <-- somme(n)
    ecrire("la somme des entiers de 1 a ", n, " est : ", resultat)
FIN 
```



