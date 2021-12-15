GROUP BY

1- SELECT COUNT(`id`), YEAR(`enrolment_date`) FROM `students` GROUP BY YEAR(`enrolment_date`);

2- SELECT COUNT(`id`), `office_address` FROM `teachers`GROUP BY `office_address`;

3- SELECT `exam_id`, AVG(`vote`) FROM `exam_student` GROUP BY `exam_id`;

4- SELECT `department_id`, COUNT(`department_id`) FROM `degrees` GROUP BY `department_id`;

JOIN

1- SELECT \* FROM `degrees` JOIN `students` ON `students`.degree_id = `degrees`.id WHERE `degrees`.name LIKE 'Corso di Laurea in Economia';

2- SELECT \* FROM `departments` JOIN `degrees`.deparments_id = `departments`.id WHERE `departments`.name LIKE `%Neuroscienze`
