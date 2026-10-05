# Objectif
Manipuler les valeurs du survey pour entrer une valeur hors scope.

## Introduction
Dans la page survey, on peut voter pour des personnes en leur attribuant des points, de 1 à 10. Le formulaire est en POST donc on ne peut pas gérer les paramètres comme avec GET dans l'url.

## Exploitation
On utilise BurpSuite et son repeater pour envoyer une requête spécifique en conservant le header. 
Après avoir définit la target on envoie le formulaire avec une valeur à 11. Le flag nous est donné comme réponse.