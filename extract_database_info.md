## Isoler un objet unique

Isole l'objet unique ayant comme id 4
SELECT * FROM aliment WHERE id = 4;

WHERE ne se limite pas que aux id.
SELECT * FROM aliment WHERE nom = "poire";


## Isolez plusieurs objets répondant à un critère de comparaison

On peut utiliser tous les opérateurs classiques :
Supérieur à ( > )
Inférieur à ( < )
Supérieur ou égal à (>=)
Et inférieur ou égal à (<=)

SELECT * FROM aliment WHERE calories < 90;


## Isolez des objets à partir d’une comparaison sur du texte

SELECT * FROM aliment ORDER BY calories ASC;

ASC => Croissant
DESC => Décroissant

On peut cumuler avec WHERE
SELECT * FROM aliment WHERE calories < 90 ORDER BY calories DESC;


## Bonnes pratiques

Au lieu d'écrire :
SELECT * FROM aliment WHERE calories < 90  AND sucre >10 ORDER BY calories DESC;

On écrit :
SELECT * 
FROM aliment 
WHERE (calories < 90)  AND (sucre >10) 
ORDER BY calories DESC;
