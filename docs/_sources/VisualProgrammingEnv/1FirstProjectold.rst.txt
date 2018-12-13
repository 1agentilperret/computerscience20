.. qnum::
   :prefix: project-one
   :start: 1


Première mission: attraper le scarabée (*the beetle*)
======================================================

.. topic:: Aperçu rapide du projet

    Vous avez options pour le premier projet qui vous accordera une note par rapport à la difficulter de l'option et de la qualité de votre programme.

Directives
-----------

Créez un programme où vous pouvez déplacer Scratch le Chat autour de la scène avec les touches fléchées.

Un deuxième sprite (le scarabée) devrait être inclus et doit rebondir continuellement sur la scène. Le but de ce petit jeu sera de déplacer Scratch pour que le chat touche le second sprite. Les fonctionnalités suivantes doivent être implémentées pour obtenir les notes maximales:

    - La musique de fond doit jouer pendant que le jeu est actif (une fois le drapeau vert enfoncé)
    - Chaque fois que le scarabée frappe le côté de la scène, un effet sonore doit être joué.
    - Lorsque Scratch atteint le scarabée:
        - Scratch devrait dire "je vous ai eu!"
        - Le scarabé devrait être placée au hasard à un nouvel emplacement et dire "Pas cette fois!", Puis reprendre son mouvement.
    - Une touche de barre d'espace devrait mettre le scarabée dans «Mode Pepsi». Lorsque vous appuyez sur la barre d'espace, le coléoptère doit se déplacer plus rapidement et se voir appliquer un effet d'image / couleur. Lorsque la barre d'espace est relâchée, son mouvement et son apparence devraient revenir à la normale.

.. note:: le bloc de détection de cyan TOUCHING peut faire référence à un autre sprite sur la scène ou au bord de la scène.

Lorsque vous avez terminé, appuyez sur le bouton PARTAGER de l'éditeur et soumettez l'URL de ce projet.

.. reveal:: extra_for_experts
    :showtitle: Dirrectives pour avoir 100%
    :hidetitle: Cacher dirrectives pour avoir 100%
    
    Modifiez le script du scarabée pour que son mouvement soit plus complexe:
        - Il devrait se déplacer en utilisant un algorithme de "randonneur aléatoire":
        - Chaque fois que le scarabée se déplace, il doit choisir l'une des trois options suivantes:
            - Tourner à droite (~ 15) et aller de l'avant
            - Tourner à gauche (~ 15) et aller de l'avant
            - Simplement avancer
        - Ne craignez pas de rebondir sur les bords de la scène.
        - Ajouter une fonctionnalité où l'utilisateur peut appuyer sur une touche pour retourner instantanément les scarabées à l'origine.
        - Créez 3 sprites Beetle distinctes qui commencent à des emplacements différents. Quand Scratch attrape un scarabée, il devrait dire "Tu m’as eu!" et disparaissent.

Évaluation
-----------

.. reveal:: eval_eighty_five
    :showtitle: Évaluation pour avoir 85%
    :hidetitle: Cacher dirrectives pour avoir 85%

    +--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Critère                                                                                                                        | oui  | non (-10%)  | un peu (-5%)|
    +================================================================================================================================+======+=============+=============+
    | La musique de fond jouer pendant que le jeu est actif                                                                          |      |             |             |
    +--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Scratch dit "je vous ai eu!" et le scarabé saute et dit "Pas cette fois!" quand ils se touchent                                |      |             |             |
    +--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Le “Mode Pepsi” est fonctionnelle lorsqu’on presse la barre d’espace et retourne à la norme quand la barre d’espace est pressé.|      |             |             |
    +--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | le scarabée rebondis et fait un son quand il touche le côté de l’écran                                                         |      |             |             |
    +--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+


+--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
| Critère                                                                                                                        | oui  | non (-10%)  | un peu (-5%)|
+================================================================================================================================+======+=============+=============+
| La musique de fond jouer pendant que le jeu est actif                                                                          |      |             |             |
+--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
| Scratch dit "je vous ai eu!" et le scarabé saute et dit "Pas cette fois!" quand ils se touchent                                |      |             |             |
+--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
| Le “Mode Pepsi” est fonctionnelle lorsqu’on presse la barre d’espace et retourne à la norme quand la barre d’espace est pressé.|      |             |             |
+--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
| le scarabée rebondis et fait un son quand il touche le côté de l’écran                                                         |      |             |             |
+--------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+



.. reveal:: eval_one_hundred
    :showtitle: Évaluation pour avoir 100%
    :hidetitle: Cacher dirrectives pour avoir 100%  
    
    
.. enlève les .. devant ceci et remplace la vidéo pour mettre la vidéo du projet dans le site

.. Si vous préférez regarder une vidéo, la `vidéo <https://www.youtube.com/watch?v=yV9GjD7-dg8>`_ suivante montre les mêmes idées que celles que j'ai décrites dans le texte ci-dessous.

.. .. youtube:: yV9GjD7-dg8
    :height: 315
    :width: 560
    :align: left
    :http: https



