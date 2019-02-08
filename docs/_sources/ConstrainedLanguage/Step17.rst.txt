Étape 17: Résoudre un labyrinthe
==================================

.. reveal:: curriculum_addressed_step_seventeen
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.


Didacticiel-*Tutorial*
-----------------------

Alors que vous commencez à réfléchir au problème suivant, je vous **recommande à nouveau** de commencer par écrire votre **pseudocode** avec du papier et un crayon.

Votre défi est de voir si vous pouvez affiner la solution de votre pseudocode pour que, lorsque vous écrivez réellement la solution Reeborg, celle-ci fonctionne du premier coup. Pour ce faire, vous devriez passer plus de temps avec le papier et le crayon qu'avec votre clavier lors de cette étape! Si vous n'avez pas de papier avec vous, demandez-en à votre enseignant.


À ton tour
------------

Ouvrez l’étape 17 de |reeborg_environment|.

Reeborg a perdu sa boîte à lunch. Reeborg jouait dans un labyrinthe et le posa avant de continuer sa promenade. Maintenant, Reeborg a faim. La boîte à lunch est représentée par le drapeau. Chaque fois que vous appuyez sur *play*, le drapeau et Reeborg commencent à un endroit aléatoire. La situation de Reeborg est la suivante:

.. image:: images/step17.gif

Ecrivez un programme pour aider Reeborg à trouver la boîte à lunch. Le secret consiste à laisser Reeborg suivre le bord droit du labyrinthe, en tournant et en se déplaçant à droite s'il le peut, en passant tout droit s'il ne peut pas tourner à droite, ou en tournant à gauche en dernier recours. Ecrivez un programme en utilisant une déclaration ``if..elif..else`` afin que Reeborg puisse manger.


.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2017" target="_blank">l'environnement Reeborg</a>