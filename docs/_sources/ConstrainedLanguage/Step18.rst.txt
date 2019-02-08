Étape 18: Le temps de la récolte revisité
===========================================

.. reveal:: curriculum_addressed_step_eighteen
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.
    - **CS20-FP3** Construct and utilize functions to create reusable pieces of code.


Didacticiel-*Tutorial*
-----------------------

Lorsque vous envisagez de rédiger une solution pour la situation suivante, veillez concidérer:

- écrire un pseudocode avec du papier et un crayon avant de commencer à coder
- utilise la bibliothèque pour stocker des fonctions que vous pourriez utiliser à nouveau (comme ``depuis la bibliothèque import va_au_debut``)
- utilisez des commentaires et des espaces (lignes vides) pour que votre code soit aussi lisible que possible par d'autres humains


À ton tour
------------

Ouvrez l'étape 18 de |reeborg_environment|.

Reeborg récolte encore des carottes. Cette fois, cependant, les jardins sont tous de tailles différentes. Les carottes poussent très bien dans certaines régions (*il y en a donc plus d'une à certains endroits*) et pas du tout à certains endroits (*il y a donc des endroits où aucune carotte ne pousse*). Reeborg peut commencer n'importe où dans le jardin et peut être orienté dans n'importe quelle direction. Un jardin possible ressemble à ceci:

.. image:: images/step18.png

La tâche de Reeborg consiste à ramasser toutes les carottes, à les déposer dans la grande corbeille à carottes au coin nord-est du jardin, puis à retourner au coin sud-ouest du jardin pour un repos bien mérité.


.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2018" target="_blank">l'environnement Reeborg</a>
