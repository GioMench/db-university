
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
    - SELECT * FROM `exams` WHERE date like '2020-06-20' and TIME(hour) > '14:00:00';
      =>Showing rows 0 - 20 (21 total, Query took 0.0087 seconds.)

6 Selezionare tutti i corsi di laurea magistrale (38)
    - SELECT * FROM `degrees` WHERE level like 'magistrale';
      =>Showing rows 0 - 24 (38 total, Query took 0.0023 seconds.)
 
7 Da quanti dipartimenti è composta l'università? (12)
    - SELECT * FROM `departments`;
      =>  Showing rows 0 - 11 (12 total, Query took 0.0006 seconds.)

8 Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
    -  SELECT * FROM `teachers` WHERE phone IS NULL;
      =>Showing rows 0 - 24 (50 total, Query took 0.0007 seconds.)


    #ATTENZIONE CORREZIONE
      molto ingegnoso mettere 265.25 per gli anni bisestili, pero' ancora piu' precisa sarebbe stata la funzione TIMESTAMPDIFF. La 4 va bene anche se LIKE e' preferibile con ricerche nel testo e l'uso di %TESTO% cosi cerchi all'interno una corrispondenza, mentre per quando e' identico il valore = funziona meglio. Idem per tutti gli altri dove hai usato like invece di uguale =.