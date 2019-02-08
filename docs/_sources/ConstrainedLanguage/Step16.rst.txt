Étape 16: Pseudocode
======================

.. reveal:: curriculum_addressed_step_sixteen
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-CP2** Use common coding techniques to enhance code elegance and troubleshoot errors throughout Computer Science 20.
    - **CS20-FP2** Investigate how control structures affect program flow.

.. index:: pseudocode

Didacticiel-*Tutorial*
-----------------------

Vous avez beaucoup appris sur la programmation de Reeborg. Félicitations! Ce que vous ne réalisez peut-être pas, c'est que vous avez beaucoup appris sur la programmation dans toutes les langues. La plupart des programmes sont une séquence d'étapes (appelée **algorithme**), entrecoupées de décisions conditionnelles et de groupes d'instructions qui se répètent.

La mise en œuvre des solutions aux tâches jusqu’à présent a demandé un peu plus de réflexion à chaque étape. Vous comprenez la question et le résultat souhaité, mais parfois, on ne sait pas tout de suite comment le faire. Lorsque vous cherchez la solution d'un problème plus complexe, il est souvent **préférable de commencer avec un crayon et du papier**.

Lorsque vous proposez la solution à un problème, écrivez les étapes dans vos propres mots avec un crayon et du papier. Cela s'appelle parfois **pseudocode** car ce ne sont pas vraiment des instructions que Reeborg (ou n'importe quel langage de programmation) pourrait utiliser. Mais cela vous aide à comprendre ce qui doit arriver. Ensuite, vous le codez -- écrivez les instructions réelles -- pour créer un programme Reeborg.

Assurez-vous de bien réfléchir à la situation suivante avant de commencer à coder. Tout d’abord, appuyez plusieurs fois sur le bouton de lecture du monde pour être sûr de bien comprendre à quoi ressemblent les mondes possibles. Déterminez maintenant l'algorithme ou la séquence d'étapes requis. Simulez ensuite dans votre imagination l'exécution du programme que vous allez écrire. Seulement si cela fait ce que vous attendez devriez-vous commencer à coder.


.. _reeborg_step_16_your_turn:

À ton tour
------------

Open Step 16 on the |reeborg_environment|.

.. image:: images/step16.png

Reeborg a été embauché pour cueillir des carottes dans plusieurs jardins. Bien que les jardins soient tous de la même taille, les carottes ont poussé à des endroits différents dans chacun des jardins. Vous devez créer un programme qui permettra à Reeborg de récolter toutes les carottes dans chacun des jardins possibles. Vous savez qu'à chaque endroit, il n'y aura que 1 ou 0 carottes.

.. note:: N'oubliez pas (d'après nos explorations dans Scratch), que vous pouvez avoir une instruction de répétition dans une autre instruction de répétition - nous avons appelé cela une **boucle imbriquée**. Déterminez comment vous pourriez utiliser une *boucle imbriquée* pour résoudre ce problème.


.. |reeborg_environment| raw:: html

   <a href="https://reeborg.cs20.ca/?lang=en&mode=python&menu=worlds/menus/sk_menu.json&name=Step%2016" target="_blank">l'environnement Reeborg</a>