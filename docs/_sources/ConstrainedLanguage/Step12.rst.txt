Étape 12: Les boucles *while*
==============================

.. reveal:: curriculum_addressed_step_twelve
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.

.. index:: while

Didacticiel-*Tutorial*
-----------------------

Lorsque nous voulons répéter certaines instructions jusqu'à ce qu'une certaine condition soit terminé, Python nous donne un moyen plus simple d’écrire cela en utilisant un nouveau mot-clé: ``while``. Par exemple, supposons que nous voulions que Reeborg se déplaçe jusqu'à ce qu'il atteind un mur. Auparavant, nous aurions pu faire quelque chose comme ce qui suit:


.. code-block:: python

    def avance_au_mur():
        if front_is_clear():
            move()

    repeat 42:
        avance_au_mur()

et espérer que 42 soit un nombre de répétitions suffisant pour atteindre un mur. En utilisant ``while``, nous pouvons écrire ce qui suit::

    while front_is_clear():
        move()

C'est tout! Plus besoin de deviner et de faire répéter quelque chose une grande nombre de fois juste pour s'assurer que ce sera suffisant.

Voici un organigramme pour ce programme simple:

.. figure:: images/flowcharts/while.jpg
   :align: center


À ton tour
-------------

Open Step 12 on the |reeborg_environment|.

.. image:: images/step12.png

L'une des tâches de Reeborg consiste à sortir le compost. Il y a cependant une quantité différente de compost dans la boîte à compost de la maison chaque fois que Reeborg doit le sortir.

Créez un programme qui permet à Reeborg de retirer le compost, puis de revenir à la maison. Reeborg doit ramasser autant de pommes pourries qu'il y a dans la boite à compost, les apporter au compost à l'extérieur, puis revenir au but (7, 8). Vous devrez utiliser des boucles ``while`` dans votre solution.


.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2012" target="_blank">l'environnement Reeborg</a>


Si vous avez des problèmes (voici une explication plus détaillée
------------------------------------------------------------------

Supposons que nous ayons::

    while condition():
        fait_1()
        fait_2()
        fait_3()

Vous pouvez penser que cela équivaut à::

    if condition():
        fait_1()
        fait_2()
        fait_3()
    if condition():
        fait_1()
        fait_2()
        fait_3()
    if condition():
        fait_1()
        fait_2()
        fait_3()
    if condition():
        fait_1()
        fait_2()
        fait_3()
    ....

ce qui revient à dire que le bloc de code est répété aussi longtemps que la condition reste ``True``. Alors, que se passe-t-il si la condition est toujours ``True``? Le bloc de code est répété infiniment et le programme prend jamais fin.

Cela serait une mauvaise expérience.

Au lieu d'utiliser cette description de blocs de code répétés,
les programmeurs décrivent cela comme une **boucle**: vous commencez par le remière instruction (``fait_1 ()``) à l'intérieur du bloc de code, continue avec tout les autres jusqu'à la dernière instruction (``fai_3()``), puis **loop back**, ou retournez à la condition juste avant le début de le bloc et voir si la condition est remplie; sinon, vous répétez le cycle. Si la condition ne devient jamais ``False``, vous continuez de répéter et finissez avec une **boucle infinie**.

Conclusion: vous voulez vous assurer que la condition deviendra
``False`` à un moment donné.