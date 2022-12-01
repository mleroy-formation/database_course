## Compter le nombre d'objets récupérés via une requête

Le mot clé COUNT permet cela, il faut l'appliquer avec la commande de type SELECT
SELECT COUNT(*) 
FROM utilisateur 
WHERE email LIKE "%gmail.com";

On peut combiner COUNT à DISTINCT pour vérifier qu'il n'y a pas de doublon : 
SELECT COUNT(DISTINCT nom) 
FROM aliment 
WHERE nom LIKE "%pomme%";


## Les alias

SELECT COUNT(DISTINCT nom)  AS "produits différents contenant le mot pomme"
FROM aliment 
WHERE nom LIKE "%pomme%";

L'alias nous permettra de donner un nom à la colonne de notre requête


## Opération sur des données chiffrées

AVG : nous donne la moyenne de la colonne sur la sélection
SUM : nous donne la somme de la colonne sur la sélection
MAX : nous donne le maximum de la colonne sur la sélection
MIN : nous donne le minimum de la colonne sur la sélection

SELECT MAX(sucre)  AS "taux de sucre maximum"
FROM aliment; 

SELECT AVG(calories) AS "calories moyennes des aliments > 30g"
FROM aliment 
WHERE calories > 30;


On peut cumuler avec la fonction ROUND pour obtenir un chiffre rond sur la moyenne :

SELECT ROUND(AVG(calories)) AS "calories moyennes des aliments > 30g"
FROM aliment 
WHERE calories > 30;
