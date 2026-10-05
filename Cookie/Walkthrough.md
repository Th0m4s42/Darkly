# Objectif
Devenir admin via le cookie.

# Introduction
Dans l'inspecteur on remarque un cookie du nom: I_am_admin avec une valeur: `68934a3e9455fa72420237eb05902327`

## Exploitation
On passe cette valeur dans crackstation et on voit que c'est une chaine en md5 se traduisant par `false`. On encrypte `true` en md5 et on remplace l'ancienne valeur par celle ci. 
On rafraîchit la page et le flag apparaît.