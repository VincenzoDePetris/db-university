- Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(`enrolment_date`), YEAR(`enrolment_date`)
FROM `students`
GROUP BY YEAR(`enrolment_date`);

- Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT `office_address`, COUNT(`office_address`)
FROM `teachers`
GROUP BY `office_address`;

- Calcolare la media dei voti di ogni appello d'esame

SELECT `exam_id`, AVG(`vote`) AS 'voto medio'
FROM `exam_student`
GROUP BY `exam_id`;

- Contare quanti corsi di laurea ci sono per ogni dipartiment

SELECT `department_id`, COUNT(`name`) AS 'Corso per ogni dipartimento'
FROM `degrees`
GROUP BY `department_id`;
