GROUP BY

1- SELECT COUNT(`id`), YEAR(`enrolment_date`) FROM `students` GROUP BY YEAR(`enrolment_date`);

2- SELECT COUNT(`id`), `office_address` FROM `teachers`GROUP BY `office_address`;

3- SELECT `exam_id`, AVG(`vote`) FROM `exam_student` GROUP BY `exam_id`;
