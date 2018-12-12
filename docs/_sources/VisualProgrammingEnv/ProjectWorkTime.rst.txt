.. qnum::
   :prefix: scratch-project
   :start: 1


Période de travail des projets
===============================

.. topic:: Aperçu rapide de la journée

    Période de travail pour mettre en pratique les concepts appris jusqu'à présent. Votre professeur vous demandera de créer un projet qui utilise la plupart des idées vues jusqu'à présent: un jeu Roch Papier Ciseau est une option intéressante.

.. reveal:: curriculum_addressed_work_period
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.



Nous n'apprendrons rien de nouveau aujourd'hui. Au lieu de cela, vous aurez le temps de travailler sur un projet qui exploite un bon nombre des idées que nous avons vues jusqu'à présent. Avant de commencer à travailler sur votre projet, cependant, vous devriez essayer le questionnaire de pratique ci-dessous pour confirmer que vous comprenez les idées que nous avons vues jusqu'à présent.

Vérifie ta compréhension
-------------------------

.. mchoice:: scratch_practice_quiz_1
    :answer_a: Le sprite actuel dirait "**Bonjour**" pendant 1 seconde, puis "**tout**" pendant 1 seconde, puis "**le monde**" pendant 1 seconde.
    :answer_b: Le sprite actuel dirait "**Bonjour**" pendant 1 seconde, puis "**le monde**" pendant 1 seconde, puis "**tout**" pendant 1 seconde.
    :answer_c: Le sprite actuel dirait "**Bonjour**" pendant 1 seconde, puis dites "**tout**" pendant 1 seconde.
    :correct: b
    :feedback_a: Non. Assurez-vous de regarder très attentivement les noms des diffusions!
    :feedback_b: Oui! L'ordre est contrôlé par les noms des diffusions, et non par ce qui est supérieur ou inférieur dans votre script.
    :feedback_c: Non. Assurez-vous de regarder très attentivement les noms des diffusions!

    Que se passerait-il lorsque vous cliquez sur le drapeau vert, étant donné le code ci-dessous?

    .. image:: images/scratch_practice_quiz_1.png


.. mchoice:: scratch_practice_quiz_2
    :answer_a: Le sprite actuel dirait "**Bonjour**" pendant 1 seconde, puis "**tout**" pendant 1 seconde, puis "**le monde**" pendant 1 seconde.
    :answer_b: Le sprite actuel dirait "**Bonjour**" pendant 1 seconde, puis "**le monde**" pendant 1 seconde, puis "**tout**" pendant 1 seconde.
    :answer_c: Le sprite actuel dira "**Bonjour**" pendant 1 seconde, puis dira "**le monde**" pour toujours.
    :correct: c
    :feedback_a: Non. Assurez-vous de regarder très attentivement les noms des diffusions!
    :feedback_b: Non. Assurez-vous de regarder très attentivement les noms des diffusions!
    :feedback_c: Oui! Etant donné que le bloc de code «**quand je reçois un alpha**» appelle soi-même, il ne cessera jamais de se répéter.

    Que se passerait-il lorsque vous cliquez sur le drapeau vert, étant donné le code ci-dessous?

    .. image:: images/scratch_practice_quiz_2.png


.. fillintheblank:: scratch_practice_quiz_3

    Given the code below, how far would the current sprite move when you click the green flag?

    .. image:: images/scratch_practice_quiz_3.png

    - :50: Oui! Etant donné que nous répétons le bloc 'avancer de 10 pas' 5 fois, cela égale à l'exécution du bloc 10 pas 5 fois.
      :5: Non. Bien qu'il y ait un bloc de répétition 5, le sprite se déplacera de **10** pas pour **chaque** répétition.
      :10: Non, puisque nous répétons le bloc 'avancer de 10 pas' 5 fois, cela éguale à l'exécution du bloc 10 pas 5 fois.
      :.*: Réessayer!


.. fillintheblank:: scratch_practice_quiz_4

    Étant donné le code ci-dessous, combien de fois entendrez-vous le miaulement lorsque vous cliquerez sur le drapeau vert?

    .. image:: images/scratch_practice_quiz_4.png

    - :3: Oui! Etant donné que l'exécution du script attend seulment les blocs "jusqu'au bout" avant de commencer le prochain son, vous n'entendrez que les deux blocs qui demande d'attendre "Jusqu'au bout" et le dernier bloc de sons son.
      :6: Non. L'exécution du script attend seulment les blocs "jusqu'au bout" avant de commencer le prochain son, vous n'entendrez que les deux blocs qui demande d'attendre "Jusqu'au bout" et le dernier bloc de sons son.
      :2: Non. L'exécution du script attend seulment les blocs "jusqu'au bout" avant de commencer le prochain son, vous n'entendrez que les deux blocs qui demande d'attendre "Jusqu'au bout" et le dernier bloc de sons son.
      :.*: Réessayer!


.. fillintheblank:: scratch_practice_quiz_5

    Étant donné le code ci-dessous, jusqu'où le sprite actuel se déplacera-t-il lorsque vous cliquez sur le drapeau vert?

    .. image:: images/scratch_practice_quiz_5.png

    - :60: Oui! Étant donné que le bloc «avance de 10 pas» se trouve dans une boucle imbriquée, il sera répété 2 fois 3 fois. Vous pouvez penser à cela comme un multiplication des valeurs de la boucle imbriquées.
      :30: Non. Étant donné que le bloc «avance de 10 pas» se trouve dans une boucle imbriquée, il sera répété 2 fois 3 fois. Vous pouvez penser à cela comme un multiplication des valeurs de la boucle imbriquées.
      :5: Non. Étant donné que le bloc «avance de 10 pas» se trouve dans une boucle imbriquée, il sera répété 2 fois 3 fois. Vous pouvez penser à cela comme un multiplication des valeurs de la boucle imbriquées.
      :.*: Réessayer! Étant donné que le «avance de 10 pas» se trouve dans une boucle imbriquée, il sera répété 2 fois 3 fois.


.. fillintheblank:: scratch_practice_quiz_6

    Étant donné le code ci-dessous, quelle serait la valeur de x après l'exécution du code suivant?

    .. image:: images/scratch_practice_quiz_6.png

    - :20: Oui! Puisque «mettre x à x + 3» se situe en dehors du bloc if si/sinon, il se produira si la valeur de «x» est inférieure ou égale à 10.
      :17: Non. Puisque «mettre x à x + 3» se situe en dehors du bloc if si/sinon, il se produira si la valeur de «x» est inférieure ou égale à 10.
      :.*: Réessayer! 


.. fillintheblank:: scratch_practice_quiz_7

    Étant donné le code ci-dessous, combien d'itérations se produiraient lorsque le code suivant est exécuté?
    
    .. image:: images/scratch_practice_quiz_6.png

    - :3: Oui! Puisque «mettre x à x + 3» se situe en dehors du bloc if si/sinon, il se produira si la valeur de «x» est inférieure ou égale à 10..
      :5: Non. Puisque «mettre x à x + 3» se situe en dehors du bloc if si/sinon, il se produira si la valeur de «x» est inférieure ou égale à 10.
      :.*: Réessayer! Puisque «mettre x à x + 3» se situe en dehors du bloc if si/sinon, il se produira si la valeur de «x» est inférieure ou égale à 10.


.. fillintheblank:: scratch_practice_quiz_8

    Étant donné le code ci-dessous, quelle serait la valeur de la variable "Mon numéro" après l'exécution de ce code?
    
    .. image:: images/set_change_test_yourself1.png

    - :99: Oui! Rappelez-vous que bloc "ajoute" ajoute simplement un montant à la valeur actuelle de la variable.
      :.*: Réessayer! Rappelez-vous que bloc "ajoute" ajoute simplement un montant à la valeur actuelle de la variable.

.. fillintheblank:: scratch_practice_quiz_9

    Étant donné le code ci-dessous, quelle serait la valeur de la variable "Mon numéro" après l'exécution de ce code?

    .. image:: images/set_change_test_yourself2.png

    - :50: Oui! N'oubliez pas que le bloc "mettre" remplace la valeur actuelle de la variable avec une valeur spécifique, peut importe ce qu'elle était avant.
      :.*: Réessayer! N'oubliez pas que le bloc "mettre" remplace la valeur actuelle de la variable avec une valeur spécifique, peut importe ce qu'elle était avant.

.. fillintheblank:: scratch_practice_quiz_10

    Étant donné le code ci-dessous, quelle serait la valeur de la variable "Mon numéro" après l'exécution de ce code?

    .. image:: images/set_change_test_yourself3.png

    - :30: Oui! N'oubliez pas que le bloc "mettre" remplace la valeur actuelle de la variable avec une valeur spécifique, peut importe ce qu'elle était avant.
      :.*: Réessayer! N'oubliez pas que le bloc "mettre" remplace la valeur actuelle de la variable avec une valeur spécifique, peut importe ce qu'elle était avant.

.. fillintheblank:: scratch_practice_quiz_11

    Étant donné le code ci-dessous, quelle serait la valeur de la variable "Mon numéro" après l'exécution de ce code?

    .. image:: images/set_change_test_yourself4.png

    - :96: Oui! N'oubliez pas que si vous utilisez une variable dans une nouvelle instruction mettre à/ajoute à, la variable contient la valeur précédente (dans ce cas, 88).
      :.*: Réessayer! N'oubliez pas que si vous utilisez une variable dans une nouvelle instruction mettre à/ajoute à, la variable contient la valeur précédente (dans ce cas, 88).

.. fillintheblank:: scratch_practice_quiz_12

    Étant donné le code ci-dessous, quelle serait la valeur de la variable "Mon numéro" après l'exécution de ce code?

    .. image:: images/set_change_test_yourself5.png

    - :12: Yes! Rappelez-vous qu’une seule branche d’un bloc si/sinon peut se produire, mais que les instructions extérieures de si/sinon s’exécutent malgré tout.
      :.*: Réessayer! Rappelez-vous qu’une seule branche d’un bloc si/sinon peut se produire, mais que les instructions extérieures de si/sinon s’exécutent malgré tout.
