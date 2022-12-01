## Insérer un objet unique dans la base de données

INSERT INTO `utilisateur` (`nom`, `prenom`, `email`)
VALUES ('Dupont', 'Eric', 'eric@gmail.com');


## Insérer plusieurs objets à la fois

INSERT INTO `utilisateur` (`nom`, `prenom`, `email`)
VALUES
('Doe', 'John', 'john@yahoo.fr'),
('Smith', 'Jane', 'jane@hotmail.com'),
('Dupont', 'Sebastien', 'sebastien@orange.fr'),
('Martin', 'Emilie', 'emilie@gmail.com');


## HELP

Noms de tables ou colonnes => Backticks (` `)
Valeurs de type TEXT ou VARCHAR => Guillemets (" ")
Valeurs de type BOOLEAN, INTEGER, FLOAT => Pas de guillemets


## Respecter la structure des tables

On fait appel aux noms des colonnes dans l'ordre qu'elle apparaîssent dans la database
On insère les valeurs dans l'ordre des colonnes également
