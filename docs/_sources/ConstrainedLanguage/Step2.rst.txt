Étape 2: Prendre et déposer des objets
=======================================

.. reveal:: curriculum_addressed_step_two
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.


Didacticiel-*Tutorial*
-----------------------

Parfois, Reeborg peut avoir besoin de prendre un objet qui se trouve sur le sol ou de poser un objet qu’il transporte. Vous pouvez utiliser la fonction ``take()`` pour indiquer à Reeborg de ramasser un objet qui se trouve sur le sol. Pour poser un objet que Reeborg est en train de porter au sol, utilisez la fonction ``put()``.

Dans l'univers Étape 2, il y a trois pissenlits sur le sol entre Reeborg et sa maison. Votre travail consiste à les ramasser, puis à les mettre à la poubelle, qui se trouve juste devant la maison, à l'adresse (5, 1).

.. image:: images/step2.png

Lorsqu'il y a un objet sur le sol, il est représenté à l'aide d'une image colorée. Le chiffre rouge situé à gauche de l'image indique le nombre d'objets de ce type. Par exemple, à l'emplacement (2, 1), il y a un pissenlit.

.. image:: images/object_on_ground.png

S'il existe un endroit spécifique où les objets doivent être déposés (également appelé objectif), il est représenté à l'aide d'une image en gris et le nombre bleu situé à droite de l'image indique le nombre d'objets que l'on s'attend à ce qu'ils soient posé à cet endroit. Par exemple, à l'emplacement (5,1), Reeborg doit poser 3 pissenlits

.. image:: images/objects_required_here.png


À ton tour
------------

Ouvrez l'étape 2 sur |reeborg_environment|.

Donnez à Reeborg les instructions appropriées pour qu’il ramasse les pissenlits, les jette à la poubelle et revienne à la maison!

.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%202" target="_blank">l'environnement Reeborg</a>