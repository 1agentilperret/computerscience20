Étape 14: Le mot-clé ``not``
===============================================

.. reveal:: curriculum_addressed_step_fourteen
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.

.. index:: not

Didacticiel-*Tutorial*
-----------------------

En Python, nous pouvons indiquer que quelque chose n'est pas vrai en écrivant ``not True`` qui est identique à ``False``. De même, ``not False`` est équivalent à ``True``.

Lorsque vous avez résolu l'étape 10, vous avez créé un programme pour qui permet à Reeborg de sauter des obstacles.

.. image:: images/hurdles2.png

Dans le cadre de votre solution pour le monde ci-dessus, vous avez peut-être créé une fonction similaire à celle-ci:

.. code-block:: python

   def cour_saute_ou_fini():
        if at_goal():
            # quelque chose
        elif front_is_clear():
            # quelque chose
        else:
            # quelque chose

Ce fragment de programme peut être réécrit en choisissant différentes combinaisons du mot clé de négation ``not`` **et** différentes combinaisons de ``if/elif/else``.

Examinez les trois exemples de code ci-dessous, en portant une attention particulière au lieu où le mot clé ``not`` se trouve **et** à ce qui est vraiment inclus dans chaque bloc de code.

.. code-block:: python

   # premier choix:

   def cour_saute_ou_fini():
        if at_goal():
            # quelque chose
        elif not front_is_clear():
            # quelque chose
        else:
            # quelque chose

   # deuxième choix ... plus compliqué

   def cour_saute_ou_fini():
        if not at_goal():
            if front_is_clear():
                # quelque chose
            else:
                # quelque chose
        else:
            # quelque chose

   # troisième choix:

   def cour_saute_ou_fini():
        if not at_goal():
            if not front_is_clear():
                # quelque chose
            else:
                # quelque chose
        else:
            # quelque chose



Vous venez de voir comment il est possible de changer l'ordre
dans lequel les conditions apparaissent dans un bloc de code ``if/elif/else`` et toujours atteindre le même objectif. Deux programmeurs différents vont souvent utilisez différentes stratégies pour obtenir le même résultat final. Il y a d'autres façons dont différents programmeurs vont écrire des programmes différents mais équivalents: en utilisant différentes fonctions.

La fonction ``front_is_clear()`` indiquera à Reeborg si un mur bloque son chemin. Il en sera de même pour **l'eau**, **les murs en briques**, **les clôtures**, etc., que nous n'avons pas encore vues, mais que nous verrons probablement dans les mondes futurs. Il existe une fonction plus spécifique au mur appelée ``wall_in_front()``; Je vous laisse deviner ce que ça fait ;).


À ton tour
------------

Ouvrez l’étape 14 de |reeborg_environment|.

.. image:: images/step14.gif

Reeborg aime aller se promener, surtout quand il se trouve autour d'un lac. Les lacs dans le voisinage de Reeborg sont tous de tailles différentes, donc Reeborg ne sait pas combien de pas il faudra pour revenir au début de la promenade. Heureusement, il arrive que Reeborg porte une banane, que vous pouvez dire à Reeborg de ``put()`` au début de la marche. Reeborg sait que la marche est finie quand il atteint à nouveau la banane.

Utilisez une déclaration ``while`` (*qui cherche la banane*) et un ``if/else`` pour que Reeborg complète sa marche autour des lacs.

.. note:: Reeborg ne peut pas utiliser une déclaration ``repeat``, car il n'a aucune idée des dimensions du lac autour de lequel il se promène.

.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2014" target="_blank">l'environnement Reeborg</a>
