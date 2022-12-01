## Création de la base de données

CREATE DATABASE nom_database;


## Utilisez une base de données avec USE et SHOW

USE nom_database;

SHOW nom_database


## Création des premières tables

CREATE TABLE utilisateur (
    id INTEGER NOT NULL AUTO_INCREMENT PRIMARY KEY,
    nom VARCHAR(100),
    prenom VARCHAR(100),
    email VARCHAR(255) NOT NULL UNIQUE
);


## Vérification de l'intégrité de la table avec SHOW tables et SHOW columns

SHOW tables;
SHOW columns FROM nom_table;

