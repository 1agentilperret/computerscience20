.. qnum::
   :prefix: reeborg-practice-quiz
   :start: 1


Premier test de pratique - ``repeat``, ``if``, ``def``
========================================================

.. reveal:: curriculum_addressed_first_practice_quiz
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.


Pour confirmer que vous comprenez les concepts majeurs que vous avez vus avec Reeborg, essayez de répondre aux questions suivantes **sans ouvrir l'environnement Reeborg**.

Question 1 - Boucles de répétitions
-------------------------------------

.. mchoice:: reeborg_repeat_loops
    :answer_a: Option 1
    :answer_b: Option 2
    :answer_c: Option 3
    :answer_d: Option 4
    :correct: c
    :feedback_a: Notez que ``move ()`` n'est pas dans la boucle de répétition. Réessayer!
    :feedback_b: Attention! Il devrait y avoir plus qu'une fleur...
    :feedback_c: Génial!
    :feedback_d: Attention! ``move ()`` ne se produira qu'une seule fois. Réessayer!

    Considérez le monde suivant, dans lequel Reeborg tient 4 fleurs:

    .. image:: images/quiz-starting-world.png
    
    Supposons que le code suivant est exécuté::

        repeat 4:
            put()
        move()

    Laquelle des images suivantes montre à quoi ressemblerait le monde une fois le code exécuté?

    **Option 1:**

    .. image:: images/quiz-optiona.png
    
    **Option 2:**

    .. image:: images/quiz-optionb.png
    
    **Option 3:**

    .. image:: images/quiz-optionc.png
    
    **Option 4:**

    .. image:: images/quiz-optiond.png
    

Question 2 - Boucles de répétitions
-------------------------------------

.. mchoice:: reeborg_repeat_loops2
    :answer_a: Option 1
    :answer_b: Option 2
    :answer_c: Option 3
    :answer_d: Option 4
    :correct: a
    :feedback_a: Génial!
    :feedback_b: Attention! Il devrait y avoir plus d'une fleur...
    :feedback_c: Notez que ``move ()`` est à l'intérieur de la répétition. Réessayer!
    :feedback_d: Attention! Les deux commandes à l'intérieur se répèteront dans l'ordre. Réessayer!
    
    **Note: Cette question est très similaire à la dernière, mais il y a un léger différence. Lire attentivement!**
    Considérez le monde suivant, dans lequel Reeborg tient 4 pâquerettes:

This question is very similar to the last one, but there is a slight change. Read carefully!**
    Consider the following world, in which Reeborg is holding 4 daisies:

    .. image:: images/quiz-starting-world.png
    
    Supposons que le code suivant est exécuté::

        repeat 4:
            put()
            move()

    Laquelle des images suivantes montre à quoi ressemblerait le monde une fois le code exécuté?

    **Option 1:**

    .. image:: images/quiz-optiona.png
    
    **Option 2:**

    .. image:: images/quiz-optionb.png
    
    **Option 3:**

    .. image:: images/quiz-optionc.png
    
    **Option 4:**

    .. image:: images/quiz-optiond.png


Question 3 - ``Repeat`` et ``if``
----------------------------

.. fillintheblank:: reeborg_repeat_if

    Supposons que le monde de départ ressemble à ceci::

    .. image:: images/quiz-starting-world2.png
    
    Le code suivant est ensuite exécuté::

        repeat 10:
            move()
            if object_here():
                take()

    Combien de pissenlits Reeborg at-il ramassé lorsque le code est terminé?

    - :6: génial!
      :10: Reeborg ne prendra qu'un pissenlit par emplacement, en raison de la fonction ``move ()`` avant le if ``object_here ()``.
      :.*: Réessayer!


Question 4 - ``Repeat`` et ``Def``
-----------------------------------

.. mchoice:: reeborg_repeat_with_functions
    :answer_a: 0
    :answer_b: 4
    :answer_c: 7
    :answer_d: Une erreur va se produire
    :correct: b
    :feedback_a: Réessayer!
    :feedback_b: Génial!
    :feedback_c: Réessayer!
    :feedback_d: Réessayer!
    
    Supposons que le monde de départ ressemble à ceci:

    .. image:: images/quiz-starting-world3.png
    
    Le code suivant est ensuite exécuté::

        def turn_right():
            repeat 3:
                turn_left()

        def turn_around():
            repeat 2:
                turn_left()

        def move_and_pick():
            move()
            take()
         
        def weeding_time():
            repeat 2:
                move_and_pick()

        repeat 4:
            move()
        turn_left()
        move()
        turn_left()

        weeding_time()
        move()
        turn_right()
        move()
        turn_right()

        weeding_time()
        move()

    Combien de pissenlits Reeborg at-il ramassé lorsque le code est terminé?

