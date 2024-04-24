
1 Selezionare tutti gli studenti nati nel 1990 (160)
    - SELECT * FROM `students` WHERE date_of_birth BETWEEN '1990-01-01' and '1990-12-31';
      => Showing rows 0 - 24 (160 total, Query took 0.0033 seconds.)

2 Selezionare tutti i corsi che valgono più di 10 crediti (479)
    - SELECT * FROM `courses` WHERE cfu > 10;
      => Showing rows 0 - 24 (479 total, Query took 0.0032 seconds.)

3 Selezionare tutti gli studenti che hanno più di 30 anni
      -SELECT * FROM `students` WHERE DATEDIFF(CURDATE(), date_of_birth) > 30*365.25;
        => Showing rows 0 - 24 (3702 total, Query took 0.0061 seconds.)

4 Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)
    - SELECT * FROM `courses` WHERE period like 'I semestre' and year like 1;
      => Showing rows 0 - 24 (286 total, Query took 0.0009 seconds.)

5 Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)
    -
 