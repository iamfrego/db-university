1 - SELECT _ FROM `university`.`students` WHERE `date_of_birth` LIKE '%1990%';
2 - SELECT _ FROM `courses` WHERE `cfu` > '10';
3 - SELECT _ FROM `students` WHERE YEAR(`date_of_birth`) < '1991';
4 - SELECT _ FROM `courses` WHERE `year` = 1 AND `period` = 'I semestre';
5 - SELECT _ FROM `exams` WHERE `hour` > '14:00:00' AND `date` = '2020-06-20';
6 - SELECT _ FROM `degrees` WHERE `level` = 'magistrale';
7 - SELECT COUNT(`id`) FROM `departments`;
8 - SELECT COUNT(`id`) FROM `teachers` WHERE phone IS NULL;
