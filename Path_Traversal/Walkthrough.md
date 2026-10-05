# Objectif 
Lire des fichiers censé être inaccessible.

## Exploitation
`http://10.171.55.130/index.php?page=../../../../../../../../etc/passwd` 
Cette faille permet de lire des fichiers du sevreur sans avoir d'accès interne initial. Ici on lit le `/etc/passwd` qui est un fichier courant à regarder en tant qu'attaquant car c'est l'endroit où les mots de passe utilisateurs sont sauvegardés. 