1. Contare quanti iscritti ci sono stati ogni anno:

```
SELECT
    COUNT(*) AS `new_students`,
    YEAR(`enrolment_date`) AS `year`
FROM `students`
GROUP BY `year`;
```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio:

```
SELECT
    COUNT(*) as `teachers_num`,
    `office_address`
FROM `teachers`
GROUP BY `office_address`;
```

3.  Calcolare la media dei voti di ogni appello d'esame:

```
SELECT
    AVG(`vote`) AS `avg_vote`,
    `exams`.`date` AS `exam_date`,
    `courses`.`name` AS `course_name`
FROM `exam_student`
INNER JOIN `exams`
ON `exams`.`id` = `exam_student`.`exam_id`
INNER JOIN `courses`
ON `courses`.`id` = `exams`.`course_id`
GROUP BY `exam_id`;
```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento:

```
SELECT
    COUNT(*) AS `degrees`,
    `departments`.`name` AS `department`
FROM `degrees`
INNER JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`
GROUP BY `department_id`;
```
