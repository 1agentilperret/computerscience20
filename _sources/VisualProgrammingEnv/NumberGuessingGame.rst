.. qnum::
   :prefix: scratch-pair-programming
   :start: 1


Jeu de devinette numérique (programmation en binôme)
=====================================================

.. topic:: Aperçu rapide de la journée

    Dans cette activité de programmation en paires, vous allez créer un jeu de devinettes qui utilise plusieurs des concepts que nous avons appris.


.. reveal:: curriculum_addressed_number_game
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.

Ce sera votre première essai dans la programmation en binôme. L'un de vous devrait être au clavier et à la souris, tandis que l'autre partenaire aide à discuter des idées. Changez de rôle toutes les 10 minutes.

.. sidebar:: Teacher Note

    Avant de demander aux élèves de créer le jeu, vous souhaiterez peut-être modéliser le jeu. L’enseignant peut jouer le rôle d’ordinateur (en choisissant un nombre aléatoire compris entre 1 et 100, en fournissant un retour trop haut / bas, et en terminant par «Vous l’avez eu en 8 essai!»), Et l’un des étudiants peut être l’utilisateur qui tente deviner le nombre.
    

Jeu de base
-------------

Pour ce projet, vous allez créer un jeu qui effectue les tâches suivantes:

- génère un nombre aléatoire de 1 à 100 et le sauver dans une variable
- répète ce qui suit jusqu'à ce que l'utilisateur devine le numéro
- oblige l'utilisateur à deviner le nombre (en utilisant le bloc **demande**)
- indique à l'utilisateur si le nombre est trop élevé ou trop bas
- félicite l'utilisateur lorsqu'il trouve le bon numéro avec un message du type "Bravo! Vous avez deviné le bon numéro en 9 essais!"

Lorsque vous avez terminé la fonctionnalité de base, levez la main et je vous dirai comment vous pouvez encore l'améliorer !

Si la description ci-dessus n’a pas de sens, voici une courte `vidéo <https://www.youtube.com/watch?v=BoSNTdrd24I>`_  de ce à quoi pourrait ressembler le jeu de devinettes de base:

.. youtube:: BoSNTdrd24I
    :height: 315
    :width: 560
    :align: left
    :http: https


Les Extensions
----------------

Voici des extras qui peuvent être ajoutés au jeu de base:

- Bien trop haute/trop basse, si la devinette est très loin du nombre réel
- très proche, mais trop haut/bas, si l’on suppose que le nombre réel est vraiment proche
- Encore trop haut/bas, si la supposition est supérieure/inférieure au nombre réel plusieurs fois de suite
- Permettre seulement un certain nombre de tentatives avant terminer le jeu
- Rôles inversés CPU/humain