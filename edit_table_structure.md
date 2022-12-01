## Ajouter un champs dans une table

ALTER TABLE aliment ADD vitamines_c FLOAT;


## Supprimer un champs dans une table

ALTER TABLE aliment DROP bio;


## Modifier un champs existant

ALTER TABLE aliment MODIFY calories FLOAT;


## Renommer un champs 

ALTER TABLE aliment CHANGE sucre sucres FLOAT;

ATTENTION : Pour renommer une colonne sur MySQL il faut spécifier le type, c'est propre UNIQUEMENT à MySQL. 
Sur un autre gestionnaire de base de données il ne faudra pas spécifier le type.
