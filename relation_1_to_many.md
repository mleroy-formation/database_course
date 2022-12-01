## Ajout d'une table

CREATE TABLE famille 
    (
        id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
        nom VARCHAR(100) NOT NULL
    );
    
INSERT INTO famille (`nom`) VALUES ('légumes');
    

## Ajout d'une relation entre 2 tables

ALTER TABLE aliment
ADD famille_id INT NULL;

ALTER TABLE aliment
ADD FOREIGN KEY (famille_id) REFERENCES famille (id)
ON DELETE CASCADE;

UPDATE `aliment` SET `famille_id` = '1' WHERE `nom` = 'haricots verts';

## Vérification

SELECT *
FROM aliment
JOIN famille ON aliment.famille_id = famille.id
WHERE aliment.nom = "haricots verts";
