# SQL - Joins & Relationships

## Description

Ce projet introduit les relations entre plusieurs tables dans une base de données SQL.

Dans les projets précédents, nous avons appris à manipuler les données dans une seule table avec les opérations CRUD. Ici, nous allons apprendre à travailler avec plusieurs tables liées entre elles.

Les bases de données réelles séparent les informations dans différentes tables afin d'organiser les données et éviter les répétitions.

## Objectifs d'apprentissage

À la fin de ce projet, vous serez capable de :

- Comprendre les relations entre les tables :
  - One-to-One (1–1)
  - One-to-Many (1–N)
  - Many-to-Many (N–N)

- Comprendre le rôle de :
  - Primary Key
  - Foreign Key

- Utiliser les jointures SQL :
  - INNER JOIN
  - LEFT JOIN
  - CROSS JOIN

- Comprendre les valeurs `NULL` dans les jointures

- Utiliser les tables de liaison (junction tables)

- Écrire des requêtes avec des sous-requêtes

## Base de données utilisée

Le projet utilise la base :

```
library.db
```

Elle contient les tables suivantes :

### authors

| Colonne | Description |
|---|---|
| id | Identifiant unique |
| name | Nom de l'auteur |
| country | Pays de l'auteur |

### books

| Colonne | Description |
|---|---|
| id | Identifiant unique |
| title | Titre du livre |
| author_id | Référence vers un auteur |
| price | Prix du livre |

### students

| Colonne | Description |
|---|---|
| id | Identifiant unique |
| name | Nom de l'étudiant |

### courses

| Colonne | Description |
|---|---|
| id | Identifiant unique |
| title | Nom du cours |

### enrollments

Table de liaison entre les étudiants et les cours.

| Colonne | Description |
|---|---|
| student_id | Identifiant étudiant |
| course_id | Identifiant cours |

## Concepts principaux

### Primary Key

Une clé primaire identifie de manière unique chaque ligne d'une table.

Exemple :

```sql
id INTEGER PRIMARY KEY
```

### Foreign Key

Une clé étrangère permet de créer une relation entre deux tables.

Exemple :

```sql
author_id REFERENCES authors(id)
```

Elle indique qu'un livre appartient à un auteur existant.

## Les JOINs

Les JOINs permettent de combiner les données provenant de plusieurs tables.

### INNER JOIN

Retourne uniquement les lignes qui possèdent une correspondance dans les deux tables.

### LEFT JOIN

Retourne toutes les lignes de la table de gauche, même si aucune correspondance n'existe.

Les valeurs manquantes apparaissent sous forme de :

```
NULL
```

### CROSS JOIN

Retourne toutes les combinaisons possibles entre deux tables.

## Exécution des fichiers SQL

Chaque tâche doit être écrite dans un fichier `.sql`.

Pour exécuter une requête :

```bash
sqlite3 library.db < fichier.sql
```

Exemple :

```bash
sqlite3 library.db < 1-inner_join.sql
```

## Règles importantes

- Chaque fichier doit contenir une seule requête SQL.
- Les résultats doivent correspondre exactement aux attentes.
- Utiliser `ORDER BY` lorsque l'ordre des résultats est demandé.
- Ne pas modifier la structure de la base sauf indication contraire.
- Les conditions de jointure doivent être écrites correctement.

## Notes sur SQLite

SQLite est utilisé pour ce projet car il est simple et léger.

À savoir :

- Les clés étrangères peuvent ne pas être activées automatiquement.
- Certaines fonctionnalités SQL peuvent différer d'autres systèmes comme PostgreSQL ou MySQL.
- SQLite ne supporte pas directement :
  - RIGHT JOIN
  - FULL OUTER JOIN

## Ressources

- SQLite SELECT
- SQLite Foreign Keys
- SQLite Expressions
- SQL JOIN concepts

## Auteur

Projet réalisé dans le cadre du programme Holberton School, par Rawan.
