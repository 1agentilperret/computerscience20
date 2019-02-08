Étape 13: If/Elif/Else *si/si alors/sinon*
===========================================

.. reveal:: curriculum_addressed_step_thirteen
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.
    - **CS20-FP3** Construct and utilize functions to create reusable pieces of code.

.. index:: if-elif-else

Didacticiel-*Tutorial*
-----------------------

Reeborg vit au Canada où il peut pleuvoir ou être ensoleillé, mais où la neige peut aussi tomber. Supposons qu'un seul d'entre eux puisse se produire à la fois. Donc, Reeborg pourrait être confronté par les choix suivants::

    if il_pleut():
        jouer_à_l_intérieur()
    elif il_neige():
        aller_skier()
    else:
        aller_nager() # supposant qu'il fait chaud!

Notez l’utilisation de ``elif`` (qui signifie «sinon si» *"else if"*) pour le choix 2. Si nous prenions en compte d’autres phénomènes météorologiques possibles, tels que grêle, tonnerre, brouillard, la pluie fine, etc., nous pourrions ajouter d’autres choix en utilisant le blocs de code ``elif: ...``.

Voici une représentation graphique des choix auxquels Reeborg est confrontée:

.. figure:: images/flowcharts/elif.jpg
   :align: center


À l'étape 10, vous avez écrit un programme pour faire sauter Reeborg. Votre programme ressemblait probablement à ceci:

.. code-block:: python

    def turn_right():
        repeat 3:
            turn_left()

    def saute_obstacle():
        #code pour faire sauter Reeborg

    repeat 5:
        move()
        saute_obstacle()

Bien que ce code fonctionne bien pour le monde des obstacles que vous avez reçu, **il échouerait si les obstacles n'étaient pas espacés de manière égale**.

Voici un squelette de programme qui devrait fonctionner pour le monde mentionné ci-dessus, à condition que vous remplissiez les parties manquantes. *Remarque: Vous pouvez trouver la fonction `fini` (qui demande à Reeborg de ne plus rien faire) utile ici.*

.. code-block:: python

   def cour_saute_ou_fini():
        # définition appropriée

   def cour_saute_ou_fini ():
        if at_goal():
            # quelque chose
        elif front_is_clear():
            # quelque chose
        else:
            # quelque chose

    repeat 42:  #nous pouvons remplacer cela par une boucle 'while' après la prochaine étape ...
        cour_saute_ou_fini()

Notez la structure des instructions ``if/elif/else``; comme mentionné ci-dessus, vous voyez que cela donne trois choix indépendants: **un seul d'entre eux sera exécuté**.

À ton tour
------------

Ouvrez l'étape 13 sur |reeborg_environment|, et copiez/collez le code suivant pour commencer votre solution:

.. code-block:: python

   def saute_obstacle():
        # définition appropriée

   def cour_saute_ou_fini ():
        if at_goal():
            fini()  #dit à Reeborg d'arrêter
        elif front_is_clear():
            # quelque chose
        else:
            # quelque chose

    repeat 42:  #nous pouvons remplacer cela par une boucle 'while' après la prochaine étape ...

        cour_saute_ou_fini()

.. image:: images/step13.png

Reeborg saute à nouveau des obstacles. Cette fois, cependant, les obstacles ne seront peut-être pas tous à la même distance. Vous devez utiliser une boucle ``repeat`` pour que Reeborg franchisse les obstacles et termine au but (12, 1). Vous **devez** utiliser une structure ``if / elif / else`` dans votre programme.

.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2013" target="_blank">l'environnement Reeborg</a>


Si vous avez des problèmes (voici une explication plus détaillée
------------------------------------------------------------------

Une série d'instructions ``if/elif/.../else`` est équivalente à
l'insertion du **premier** bloc de code qui renvoi un ``True``. Ainsi::

    if False:
        fait_1()
    elif True:
        fait_2()
    elif True:
        fait_3()
    else:
        fait_4()

est équivalent à::

    fait_2()

tandis que::

    if False:
        fait_1()
    elif False:
        fait_2()
    elif False:
        fait_3()
    else:
        fait_4()

est équivalent à::

    fait_4()

etc.

