## 1. Selezionare tutti gli studenti nati nel 1990 (160)

- SHOW databases;
<!-- per vedere tutti i database presenti nel mio phpMyAdmin -->

- USE `91_university`;
<!-- per utilizzare un determinato database -->
- SHOW tables;
<!-- per mostare tutte le tabelle presenti nel database 
NB: se nel terminale faccio tutto insieme ossia:
SHOW databases;
USE `91_university`;
SHOW tables; 
funziona ma se uso SHOW tables; separatamente mi da errore 🤬-->
- DESCRIBE `students`;
<!-- Per vedere come è formata una tabella di una colonna esempio di students
NB: come con SHOW tables da errore se non lo si fa tutto insieme quindi:
SHOW databases;
USE `91_university`;
SHOW tables; 
DESCRIBE `students` -->

- SELECT * FROM `students` WHERE `date_of_birth` LIKE '1990%'


## 2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `courses`;
- SELECT * FROM `courses` WHERE `cfu` > 10;

## 3. Selezionare tutti gli studenti che hanno più di 30 anni

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `students`;
- SELECT * FROM `students` WHERE `date_of_birth` BETWEEN '1970-01-01' AND '1993-01-01' ORDER BY `date_of_birth` ASC;
- risultati (3502)


## 4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `courses`;
- SELECT * FROM `courses` WHERE `period` LIKE 'I %' AND `year` = 1;


## 5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del20/06/2020 (21)

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `exams`;
- SELECT * FROM `exams` WHERE `date` = '2020-06-20' AND `hour` >= '14%';

## 6. Selezionare tutti i corsi di laurea magistrale (38)

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `degrees`;
- SELECT * FROM `degrees` WHERE `level` = 'magistrale';


## 7. Da quanti dipartimenti è composta l'università? (12)

- SHOW databases;
- USE `91_university`;
- SHOW tables;
- DESCRIBE `departments`;
- SELECT * FROM `departments` WHERE `id`;


## 8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)