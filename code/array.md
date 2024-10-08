1. [Introduction](../README.md)
1. [Les variables](./variables.md)
1. [Les conditions](./conditions.md)
1. [Les boucles](./whileAndfor.md)  
1. Les tableaux  ←
1. [Les fonctions](./function.md)
1. [Aller plus loin](./allerplusloin.md)


# Les tableaux

Grâce aux tableaux, nous allons pouvoir complexifier nos algorithmes et éviter d'avantage les répétitions. À l'inverse des variables classiques, les tableaux permettent de stocker plusieurs valeurs dans une variable. Imaginons qu'on a une classe de 25 ~~élèves~~ apprenants. Si on veut pouvoir stocker les prénoms de chaque apprenant pour s'en servir plus tard, on est obligé de faire ceci : 

````
DEBUT
    eleve1 = "Serge"
    eleve2 = "Marie"
    eleve3 = "Pierre"
    eleve4 = "Odile"
    ...
    ECRIRE eleve1, " est dans la classe de Dev"
    ECRIRE eleve2, " est dans la classe de Dev"
    ECRIRE eleve3, " est dans la classe de Dev"
    ECRIRE eleve4, " est dans la classe de Dev"
FIN
````
Cela ne fait pas très D.R.Y n'est-ce pas ? L'utilisation des tableaux et des boucles nous aident à améliorer notre code. 

Un tableau s'écrit comme ceci :
````
eleve = ["Serge","Marie", "Pierre", "Odile"]
````
On mets toutes les valeurs entre les [ ]. Pour récupérer la valeur, on doit déterminer un index. Si on veut récuperer la valeur "Serge", on doit le faire comme ceci ``ECRIRE eleve[1]``, le chiffre 1 étant l'index. Si on veut récuperer "Marie", dans ce cas on mettra l'index à 2 ``ECRIRE eleve[2]`` etc.

Essayez !
````
\\ Module principal
DÉBUT
    eleve = ["Serge","Marie", "Pierre", "Odile"]         
    ECRIRE eleve[1]  
FIN         
````

Grâce aux boucles, nous allons pouvoir parcourir l'ensemble du tableau en écrivant l'instruction une seule fois. Essayez ce bout de code !

````
\\ Module principal
DÉBUT
    eleve = ["Serge","Marie", "Pierre", "Odile"]
    POUR nombre = 1  JUSQU'À 4 FAIRE      
        ECRIRE eleve[nombre], "est dans la classe de Dev"
    FINPOUR 
FIN  
````
Ici c'est la variable ``nombre`` qui est l'index du tableau ``eleve``.


## Tableaux multi-dimensionnels
On peut également imbriquer des tableaux. Imaginons que nous souhaitons stocker dans un tableau tous les apprenants de Dev par promo. Donc un tableau = une promo. Pour ce faire on va créer un tableau apprenant

````
apprenants = []
````

Dans ce tableau nous allons y stocker un autre tableau avec les apprenants de la promo 2024. 

````
apprenants = [["David", "Justine", "Valentin","Axel"]]
````

Ensuite imaginons que nous souhaitons rajouter les apprenants de 2023.

````
apprenants = [["David", "Justine", "Valentin","Axel"], ["Julie", "Stéphane", "Mostapha", "Claudiu", "Son"]]
````
Comme vous pouvez le voir, on rajoute un tableau séparé par une virgule. Nous avons donc un tableau qui contient lui même deux tableaux.

Si on veut récupérer la première valeur du premier tableau nous devons procéder comme ceci : 

````
ECRIRE apprenants[1][1]
````
Ce qui nous donnera : "David". Si on veut récupérer le premier élément du deuxième tableau. On entre donc dans le premier tableau et on choisit le premier élément.

````
ECRIRE apprenants[2][1]
````

Pour parcourir l'ensemble de ces tableaux, nous allons faire une boucle dans une boucle... Vous commencez à avoir mal de tête ? C'est normal, ne vous inquiétez pas mais c'est pas aussi compliqué que ça en à l'air.



On crée donc une première boucle qui va parcourir le 1er tableau. Dans cette même boucle on imbrique une seconde boucle qui va parcourir les deux autres tableaux... Vous suivez ? 


![While nesting](https://media0.giphy.com/media/3oKGztUyVs2DTkhGUM/giphy.gif?cid=ecf05e475bb5e19d706464747717fdda)

Voici un exemple de code, essayez ! 

````
\\ Module principal
DÉBUT
    apprenants = [["David", "Justine", "Valentin","Axel", "Redouane"], ["Julie", "Stéphane", "Mostapha", "Claudiu", "Son"]]
  
    POUR i = 1 JUSQU'À 2 FAIRE
        POUR y = 1 JUSQU'À 5 FAIRE
            ECRIRE apprenants[i][y] 
        FINPOUR 
    FINPOUR
FIN  
````
La première boucle sera incrémentée 2 fois car il y a 2 tableaux.
La seconde boucle sera incrémentée 5 fois car chaque tableau contient 5 éléments. Bon allez c'est pas compliqué si ? 




## Exercices 

1. Créer un tableau qui contient 5 prénoms. Ensuite faire en sorte d'afficher cette phrase  : " LE_PRENOM est dans la classe de Dev"
2. Reprendre le tableau précédent et utiliser ce tableau ci-dessous. Cette fois faire en sorte d'afficher une competence par éléve. 
``competence = ["html", "css", "javascript", "php", "Java"]``
3. Créer un algorithme qui affiche le nombre le plus grand de ces tableaux. ``nombres = [[18,55], [29,13], [-2,15],[66,44]]``
4. Reprendre ce tableau ``apprenants = [["David", "Justine", "Valentin","Axel", "Redouane"], ["Julie", "Stéphane", "Mostapha", "Claudiu", "Son"]]``. Faire en sorte que le premier tableau affiche "PRENOM est chez les 2024". Le second tableau devra afficher "PRENOM est chez les 2023".


&nbsp; 
    
**Chapitre suivant**  
-> [Les fonctions](./function.md)  

