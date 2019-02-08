Étape 9: Répéter ees instructions
=======================================

.. reveal:: curriculum_addressed_step_nine
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.
    

.. index:: repeat

Didacticiel-*Tutorial*
-----------------------

Nous constatons souvent que nous souhaitons répéter une série d'instructions un nombre de fois déterminé. Par exemple, à l'étape 8, vous deviez demander à Reeborg de faire la même chose plusieurs fois. Il existe un moyen de faire cela en Python ... mais il a trop de nouveaux concepts à expliquer pour le moment. Je vais simplement vous montrer le code python et vous présenter immédiatement la commande ``repeat``, un remplacement plus simple, unique au monde de Reeborg. La méthode standard est connue sous le nom de boucle *for loop* (que nous utiliserons plus tard dans le cours) et s’écrit comme suit:

.. code-block:: python

    for i in range(n):
        # mettre
        # instructions
        # ici

Dans le monde de Reeborg, nous pouvons écrire une *boucle* ``repeat`` comme ceci:

    repeat n:    # où n est un nombre naturel, comme 3 ou 7
        # mettre
        # instructions
        # ici

.. note::

   L’utilisation de ``repeat`` ne fonctionnera pas dans les programmes Python destinés à être exécutés en dehors du monde de Reeborg.

Une **boucle** est un bloc d'instructions qui est répété. Chaque fois que la boucle est répétée est appelée une itération, le code ci-dessous aurait donc 4 itérations.

Le code suivant fera que Reeborg trace un carré::

    repeat 4:
        move()
        turn_left()

En utilisant ``repeat``, nous pouvons réécrire certaines définitions de fonctions sans avoir à répéter les instructions::

    def turn_right():
        repeat 3:
            turn_left()

Vous pouvez aussi ajuster le code que vous avez enregistré dans l'onglet **Bibliothèque** pour utiliser le bloc de répétition.

.. admonition:: Pour les éducateurs

    La raison que nous présentons ``repeat`` en même temps et au lieu de la notation standard de Python et d'évite avoir à introduire 4 concepts en même temps (boucles, variables comme dans ``for i in range(n):``, des fonctions intégrées telles que ``range`` ainsi que le concept d'``arguments de fonctions``).

    De par sa conception, le ``n`` dans le ``repeat n`` **doit** être un entier; cela ne peut pas être une variable. Lorsque les étudiants étudient les variables, ils doivent apprendre la syntaxe Python appropriée pour faire des boucles et oublier la répétition non standard.

À ton tour
------------

Ouvrez l'étape 9 sur |reeborg_environment|.

.. image:: images/step9.png

Ajustez la solution que vous avez créée pour l’étape 8 en utilisant deux boucles de répétition cette fois. Le monde n’a pas changé depuis l’étape 8, mais votre solution devrait être beaucoup plus éléguante. N'oubliez pas d'utiliser des commentaires et des espaces pour augmenter la lisibilité de votre solution!

.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%209" target="_blank">l'environnement Reeborg</a>