# Objectif 

Exploiter l'espace commentaire

## La Faille XSS Stockée

Le code injecté est enregistré de manière permanente sur le serveur (dans une base de données, un forum ou un champ de commentaires). Il s'exécute automatiquement pour chaque visiteur qui charge la page concernée. Ici pour avoir le flag il suffit que le mot ```script``` soit présent dans l'espace commentaire.


| Étape | Faille | Référence |
|-------|--------|-----------|
| Exploitation de l'espace commentaire | Neutralisation incorrecte des entrées lors de la génération de pages web | CWE-79 |