## Extraire des informations via une relation 1 to many

SELECT * 
FROM utilisateur
JOIN langue
ON utilisateur.langue_id = langue.id;


## Extraire des informations via une relation many to many

SELECT *
FROM utilisateur
JOIN utilisateur_aliment ON (utilisateur.id = utilisateur_aliment.utilisateur_id)
JOIN aliment ON (aliment.id = utilisateur_aliment.aliment_id);
