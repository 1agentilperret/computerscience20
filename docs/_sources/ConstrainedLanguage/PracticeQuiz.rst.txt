.. qnum::
   :prefix: reeborg-second-quiz
   :start: 1


Deuxième test de pratique
================================

.. reveal:: curriculum_addressed_practice_quiz_reeborg
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.
    - **CS20-FP3** Construct and utilize functions to create reusable pieces of code.

Pour confirmer que vous comprenez les concepts majeurs que vous avez vus avec Reeborg, essayez de répondre aux 4 premières questions **sans ouvrir l'environnement Reeborg**.

Question 1 - Boucle ``While`` 
------------------------------

.. mchoice:: reeborg_while_loops
    :answer_a: est
    :answer_b: sud
    :answer_c: ouest
    :answer_d: nord
    :correct: d
    :feedback_a: réessayez!
    :feedback_b: réessayez!
    :feedback_c: réessayez!
    :feedback_d: Génial!

    Reeborg est face à l'est. Le code suivant est ensuite exécuté::

        while not is_facing_north():
            turn_left()

    À quelle direction le robot fait-il face maintenant?


Question 2 - Boucles ``While`` et ``Repeat``
----------------------------------------------

.. mchoice:: reeborg_while_and_repeat
    :answer_a: est
    :answer_b: sud
    :answer_c: ouest
    :answer_d: nord
    :correct: c
    :feedback_a: réessayez!
    :feedback_b: réessayez!
    :feedback_c: Génial!
    :feedback_d: réessayez!

    Reeborg est face à l'est. Le code suivant est ensuite exécuté::

        while not is_facing_north():
            turn_left()
        repeat 5:
            turn_left()

    À quelle direction le robot fait-il face maintenant?


Question 3 - ``Boucles`` et ``if``
------------------------------------

.. fillintheblank:: reeborg_while_repeat_if

    Reeborg se situe dans un monde où chaque carré a 3 carottes, qui ressemble à ceci:

    .. image:: images/practice_quiz_start.png

    Le code suivant est ensuite exécuté::

        repeat 8:
            if object_here():
                repeat 2:
                    take()
            move()

    Combien de carottes a-t-il Reeborg maintenant?

    - :16: Génial!
      :8: N'oubliez pas qu'il y a un ``repeat 2`` à l'intérieur de le ``repeat 8``.
      :.*: réessayez!


.. reveal:: reveal_practice_quiz_q3
    :showtitle: Aide sur le traçage
    :hidetitle: Masquer l'aide

    Si vous avez passé du temps à travailler ce code par vous-même et que vous ne parvenez toujours pas à trouver la solution appropriée, il peut être utile |reeborgq3|. Vous pouvez copier/coller le code ci-dessus dans le monde et parcourir le code ligne par ligne.


.. |reeborgq3| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&url=worlds/sk/second-practice-quiz-q3.json&name=PracticeQuizQ3" target="_blank">d'ouvrir ce monde dans l'environnement Reeborg</a>

Question 4 - ``Boucles`` et ``If/Else``
-----------------------------------------

.. fillintheblank:: reeborg_while_repeat_if_else

    Reeborg tient une grande poignée de carottes et envisage de les planter alors qu'il se promène dans un monde qui ressemble à ceci:

    .. image:: images/quiz_if_else_start.png

    Le code suivant est ensuite exécuté::

        repeat 7:
            if front_is_clear():
                move()
            else:
                turn_left()
                put()

    Combien de carottes Reeborg a-t-il plantées lorsque le code est terminé?

    - :1: Génial!
      :2: Attention! Rappelez-vous que le ``else`` n'inclut pas le ``move``.
      :.*: réessayez!

.. reveal:: reveal_practice_quiz_q4
    :showtitle: Aide sur le traçage
    :hidetitle: Masquer l'aide

    Si vous avez passé du temps à travailler ce code par vous-même et que vous ne parvenez toujours pas à trouver la solution appropriée, il peut être utile |reeborgq4|. Vous pouvez copier/coller le code ci-dessus dans le monde et parcourir le code ligne par ligne.

.. |reeborgq4| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&url=worlds/sk/second-practice-quiz-q4.json&name=PracticeQuizQ4" target="_blank">d'ouvrir ce monde dans l'environnement Reeborg</a>

Question 5 - Image de réflexion
--------------------------------

La pièce (ci-dessous) a des alcôves à gauche et à droite. Certaines des alcôves contiennent des fleurs. Pour chaque alcôve sur le côté gauche contenant une fleur, amenez Reeborg à déplacer la fleur vers l'alcôve opposée du côté droit. Un monde de départ possible pourrait ressembler à ceci:

Ouvrez le |alcove1| et créer une solution à ce problème!

.. image:: images/practice_quiz_alcove_start.png

**Ne regardez pas** à cet exemple de solution à moins que vous avez déjà fini de créer votre propre solution! 

.. reveal:: reveal_practice_quiz_solution
    :showtitle: Voir la Solution
    :hidetitle: Masquer la Solution

    Puisque toutes les distances dans le monde restent exactement les mêmes à chaque fois, ce problème peut être résolu en utilisant uniquement des boucles ``repeat``. Veuillez noter qu'il existe de nombreuses solutions possibles à ce problème. En voici une::
    

        think(0)

        def turn_around():
            repeat 2:
                turn_left()

        def turn_right():
            repeat 3:
                turn_left()

        def move_daisy():
            take()
            turn_around()
            repeat 6:
                move()
            put()
            turn_around()
            repeat 5:
                move()
            turn_right()

        repeat 6:
            move()
            turn_left()
            move()
            if object_here():
                move_daisy()
            else:
                turn_around()
                move()
                turn_left()
            if front_is_clear():
                move()


.. |alcove1| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&url=worlds/sk/practice-quiz-alcove.json&name=PracticeQuizAlcove" target="_blank">monde de pratique de l'image de réflexion</a>

Question 6 - Image de réflexion - 2e partie
---------------------------------------------

Cette fois, la distance entre l'alcôve à droite et à gauche n'est pas cohérente (C.À.D., les alcôves peuvent être différentes les unes des autres). Encore une fois, pour chaque alcôve contenant une fleur du côté gauche, amenez Reeborg à déplacer la fleur dans l'alcôve opposée du côté droit. Un monde de départ possible pourrait ressembler à ceci:

Ouvrez le |alcove2| et créer une solution à ce problème!
.. image:: images/practice_quiz_alcove2_start.png

** Ne regardez pas ** cet exemple de solution à moins que vous avez déjà fini de créer votre propre solution!

.. reveal:: reveal_practice_quiz_solution2
    :showtitle: Voir la Solution
    :hidetitle: Masquer la Solution

    Comme il y a une distance inconnue à parcourir, vous devrez utiliser une boucle `while`, au lieu de simplement une boucle `repeat`. Voici une solution possible ::

        think(0)

        def turn_around():
            repeat 2:
                turn_left()

        def turn_right():
            repeat 3:
                turn_left()

        def backup():
            turn_around()
            move()
            turn_around()

        def move_daisy():
            take()
            turn_around()
            while front_is_clear():
                move()
            put()
            turn_around()
            while front_is_clear():
                move()
            backup()
            turn_right()

        repeat 6:
            move()
            turn_left()
            move()
            if object_here():
                move_daisy()
            else:
                turn_around()
                move()
                turn_left()
            if front_is_clear():
                move()


.. |alcove2| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&url=worlds/sk/practice-quiz-alcove2.json&name=PracticeQuizAlcove2" target="_blank">Monde de la pratique de l'image de réflection</a>
