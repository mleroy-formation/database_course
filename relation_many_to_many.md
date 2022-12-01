## Ajout d'une nouvelle table

CREATE TABLE lieu (
id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
nom VARCHAR(100) NOT NULL,
type VARCHAR(100) NOT NULL
);

INSERT INTO `lieu` (`nom`, `type`) VALUES ('Carrefour', 'supermarché');


## Ajout de la table de liaison

CREATE TABLE aliment_lieu (
aliment_id INT NOT NULL,
lieu_id INT NOT NULL,
FOREIGN KEY (aliment_id) REFERENCES aliment (id) ON DELETE RESTRICT ON UPDATE CASCADE,
FOREIGN KEY (lieu_id) REFERENCES lieu (id) ON DELETE RESTRICT ON UPDATE CASCADE,
PRIMARY KEY (aliment_id, lieu_id)
);

INSERT INTO `aliment_lieu` (`aliment_id`, `lieu_id`) VALUES ('11', '1');


## Vérification

SELECT *
FROM  aliment
JOIN aliment_lieu ON aliment.id = aliment_lieu.aliment_id
JOIN lieu ON lieu.id = aliment_lieu.lieu_id
WHERE aliment.id = 11;
