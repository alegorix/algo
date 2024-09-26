1. [Introduction](../README.md)
1. [Les variables](./variables.md)
1. [Les conditions](./conditions.md)
1. [Les boucles](./whileAndFor.md)  
1. [Les tableaux](./array.md) 
1. [Les fonctions](./function.md)
1. Aller plus loin ←



## Allons plus loin !


Demandons à l’utilisateur d’entrer une valeur (entière) en degrés Celsius (°c) :

* Si la température est supérieure à 5°c, lui dire qu’il n’y a pas de danger !
* Si la température est comprise entre 1 et 5°c inclus, lui dire qu’il existe un danger de plaques de verglas isolées !
* Si la température est en dessous de 1°c inclus, lui dire qu’il existe un danger de verglas généralisé !

On demande d’écrire un algorithme en utilisant un organigramme

## Création de notre organigramme
![Organigramme_temperature](./temperature_organigr_pos.png)
### >>> Essayez de le faire en pseudo-code


<details>
    <summary>Solution</summary>

````
\\ Module principal
DÉBUT
    ECRIRE "Entrez une température :"
    LIRE temp
    SI temp > 5 ALORS 
    ECRIRE "Pas de danger"
    SINON SI temp > 1 ALORS
    ECRIRE "Risque de verglas isolé"
    SINON
    ECRIRE "Risque de verglas généralisé"
    FINSI
FIN
````
</details>    

&nbsp; 




## Ecriture en Python
Analysez le code ci-dessous, on dirait du pseudo-code amélioré ? Non ?
````
print(" Entrez la température : ")
temp=int(input())
if temp > 5:
    print("Pas de danger")
elif temp > 1:
    print("Risque de verglas isolé")
else:
    print("Risque de verglas généralisé")
````

## Idem mais en HTML (et avec du Javascript)
````
<!DOCTYPE html>
<html>
  <head>
    <title>Température</title>
  </head>
  <body>
    <label for="temperature">Entrez la température :</label>
    <input type="number" id="temperature">
    <button onclick="checkTemperature()">Vérifier</button>
    <p id="result"></p>

    <script>
      function checkTemperature() {
        var temp = document.getElementById("temperature").value;
        if (temp > 5) {
          document.getElementById("result").innerHTML = "Pas de danger";
        } else if (temp > 1) {
          document.getElementById("result").innerHTML = "Risque de verglas isolé";
        } else {
          document.getElementById("result").innerHTML = "Risque de verglas généralisé";
        }
      }
    </script>
  </body>
</html>
````
