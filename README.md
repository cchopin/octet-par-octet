# Le poids des types

Page interactive pour expliquer aux développeurs l'impact du choix des types de données dans SQL Server : taille des lignes et des pages, clé primaire int ou GUID, index secondaires, mémoire réservée pour les tris, Unicode, numéros de téléphone, types de date et requêtes sargables.

## Contenu

| Section | Sujet |
|---|---|
| 00 | Les bases : pages de 8 Ko, lecture par page, clé primaire, mémoire réservée |
| 01 | Atelier : construire deux versions d'une table par glisser-déposer et comparer leur poids |
| 02 | Clé primaire : int IDENTITY, NEWID(), NEWSEQUENTIALID(), page splits, clé recopiée dans les index |
| 03 | Tri et mémoire : estimation des colonnes variables, memory grant, débordement dans tempdb |
| 04 | Texte et Unicode : varchar, nvarchar, collation, collation UTF-8 |
| 05 | Le numéro de téléphone, cas d'école |
| 06 | Dates et heures : types disponibles, précision, piège de 23:59:59.999 |
| 07 | Requêtes sargables : Index Seek et Index Scan, pièges des ORM |
| 08 | Mémo des tailles et lexique |

## Utilisation

Aucune dépendance ni étape de build : ouvrir `index.html` dans un navigateur suffit. Seules les polices sont chargées depuis Google Fonts, avec des polices système en repli.

## Publication sur GitHub Pages

1. Pousser le dépôt sur GitHub.
2. Dans le dépôt : Settings, puis Pages.
3. Source : « Deploy from a branch », branche `main`, dossier `/ (root)`.
4. La page est publiée à l'adresse `https://<compte>.github.io/<depot>/` après une à deux minutes.

## Limites

Les calculs sont simplifiés à but pédagogique : tables sans compression, colonnes NOT NULL, textes stockés dans la ligne. Les estimations de mémoire sont des ordres de grandeur.
