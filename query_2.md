## Group by
1 Contare quanti iscritti ci sono stati ogni anno

    - SELECT YEAR(enrolment_date) AS anno, COUNT(*) AS numero_iscritti FROM `students` GROUP BY YEAR(enrolment_date);
    => Showing rows 0 - 3 (4 total, Query took 0.0049 seconds.)
       => anno  n_iscritti
          2018         912
          2019        1709
          2020        1645
          2021         734 


2 Contare gli insegnanti che hanno l'ufficio nello stesso edificio

    - SELECT COUNT(id), `office_address` FROM`teachers` GROUP BY `office_address`;
    =>  Showing rows 0 - 24 (29 total, Query took 0.0043 seconds.)
        => count(id)    office_address
            1              Borgo Demis 1
            8              Borgo Elga 89
            4              Borgo Elio 234 Piano 4
            1              Borgo Ippolito 5 Piano 5
            ecc..
            1              Via Elga 7 Piano 4


3 Calcolare la media dei voti di ogni appello d'esame

    - SELECT `exam_id`, AVG(vote) AS average FROM exam_student GROUP BY `exam_id`;
    => Showing rows 0 - 24 (4078 total, Query took 0.0053 seconds.)
       => exam_id       average
                1       16.8824
                2       16.4615
                3       20.3333
                ecc..
                36      20.1818

4 Contare quanti corsi di laurea ci sono per ogni dipartimento

    - SELECT COUNT(id), `department_id` FROM `degrees` GROUP BY `department_id`;
    => Showing rows 0 - 11 (12 total, Query took 0.0022 seconds.)
       => count(id)     department_id
                10                 1
                 4                 2
                 4                 3
                 9                 4
                 ecc..
                 7                12