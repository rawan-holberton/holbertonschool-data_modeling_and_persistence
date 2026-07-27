# SQL - CRUD Operations

## Description

Ce projet a pour objectif de découvrir les bases du SQL en utilisant SQLite. Il permet de manipuler une base de données contenant des livres en réalisant les opérations CRUD (Create, Read, Update, Delete).

Les requêtes SQL sont écrites dans des fichiers `.sql` et exécutées avec SQLite.

## Objectifs

À la fin de ce projet, vous serez capable de :

- Comprendre le modèle relationnel (tables, lignes, colonnes)
- Écrire des requêtes SQL simples
- Ajouter des données avec `INSERT`
- Lire des données avec `SELECT`
- Modifier des données avec `UPDATE`
- Supprimer des données avec `DELETE`
- Filtrer les résultats avec `WHERE`
- Trier les résultats avec `ORDER BY`
- Limiter les résultats avec `LIMIT`
- Utiliser les fonctions d'agrégation (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)
- Regrouper les données avec `GROUP BY`

## Base de données

Le projet utilise une base SQLite contenant une table `books`.

| Colonne | Type |
|---------|------|
| id | INTEGER |
| title | TEXT |
| author | TEXT |
| genre | TEXT |
| price | REAL |
| stock | INTEGER |
| published_year | INTEGER |

## Exécution

Exécuter une requête SQL :

```bash
sqlite3 books_dataset.db < fichier.sql
```

Exemple :

```bash
sqlite3 books_dataset.db < 0-select_all.sql
```

## Contraintes

- Ubuntu 20.04
- SQLite 3.x
- Une seule requête SQL par fichier (sauf indication contraire)
- Ne pas utiliser de `JOIN` ni de sous-requêtes
- Utiliser `ORDER BY` lorsque l'ordre des résultats est demandé

## Auteur

Projet réalisé dans le cadre du programme Holberton School, par Rawan.
