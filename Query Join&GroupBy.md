GROUP BY

1- SELECT COUNT(id), YEAR(enrolment_date) FROM students GROUP BY YEAR(enrolment_date);

2- SELECT COUNT(id), office_address FROM teachersGROUP BY office_address;

3- SELECT exam_id, AVG(vote) FROM exam_student GROUP BY exam_id;

4- SELECT department_id, COUNT(department_id) FROM degrees GROUP BY department_id;

Join

JOIN

1- SELECT \* FROM degrees JOIN students ON students.degree_id = degrees.id WHERE degrees.name LIKE 'Corso di Laurea in Economia';

2- SELECT \* FROM departments JOIN degrees.deparments_id = departments.id WHERE departments.name LIKE %Neuroscienze

3- SELECT \* FROM teachers JOIN course_teacher ON course_teacher.teacher_id = teachers.id WHERE course_teacher.teacher_id LIKE 44

4- SELECT students.surname, students.name, degrees.name, degrees.level, degrees.email, degrees.website, departments.name FROM students JOIN degrees ON students.degree_id = degrees.id JOIN departments ON degrees.department_id = departments.id ORDER BY students.surname, students.name

5- SELECT degrees.name, courses.name, teachers.name, teachers.surname FROM degrees JOIN courses ON degrees.id = courses.degree_id JOIN course_teacher ON course_teacher.course_id = courses.id JOIN teachers ON teachers.id = course_teacher.teacher_id ORDER BY degrees.name

6- SELECT DISTINCT teachers.name, teachers.surname, departments.name FROM teachers JOIN course_teacher ON teachers.id = course_teacher.teacher_id JOIN courses ON course_teacher.course_id = courses.id JOIN degrees ON courses.degree_id = degrees.id JOIN departments ON degrees.department_id = departments.id WHERE departments.name = 'Dipartimento di Matematica'\

7- SELECT DISTINCT teachers.name AS teacher_name, teachers.surname AS teacher_surname, departments.name AS department_name FROM teachers JOIN course_teacher ON teachers.id = course_teacher.teacher_id JOIN courses ON course_teacher.course_id = courses.id JOIN degrees ON courses.degree_id = degrees.id JOIN departments ON degrees.department_id = departments.id WHERE departments.name = 'Dipartimento di Matematica';

8- SELECT COUNT(exams.id), students.name, students.surname, courses.name FROM students JOIN exam_student ON students.id = exam_student.student_id JOIN exams ON exams.id = exam_student.exam_id JOIN courses ON courses.id = exams.course_id GROUP BY exam_student.student_id, exams.course_id;
