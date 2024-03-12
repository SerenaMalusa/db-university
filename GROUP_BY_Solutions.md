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

```
