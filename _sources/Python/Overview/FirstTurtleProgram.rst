.. qnum::
   :prefix: first-turtle
   :start: 1


Notre premier programme de Turtues/*Turtle*
=============================================

.. topic:: Aperçu rapide de la journée

    Apprenez à dessiner en Python en utilisant le module turtle/*turtle*.


.. reveal:: curriculum_addressed_first_turtle_program
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.


.. index:: turtle

Il existe de nombreux *modules* en Python qui fournissent des fonctionnalités très puissantes que nous pouvons utiliser dans nos propres programmes. Certains d'entre eux peuvent envoyer un courriel ou récupérer des pages Web. D'autres nous permettent d'effectuer des calculs mathématiques complexes. Nous avons déjà utilisé un module, appelé ``easygui_qt``, qui nous permettait d'utiliser des fenêtres contextuelles lorsque nous demandions une saisie de l'utilisateur. Aujourd'hui, nous allons présenter un module qui nous permet de créer un objet de données appelé **turtle** pouvant être utilisé pour dessiner des images. *Le module turtle est très similaire à la fonctionnalité du stylo que nous avons explorée avec Scratch! * Notez que le module ``turtle`` fait partie de l'installation standard de Python, vous n'avez donc pas besoin de l'installer avant de l'utiliser.

Turtle Graphics, comme il est connu, est basé sur une métaphore très simple. Imaginez que vous avez une tortue qui comprend l'anglais. Vous pouvez dire à votre tortue de faire des commandes simples telles que avancer et tourner à droite. Lorsque la tortue se déplace, si sa queue touche le sol, elle tracera une ligne (laissant une trace derrière) à mesure qu'elle se déplacera. Si vous dites à votre tortue de relever la queue, elle peut toujours se déplacer mais ne laissera pas de trace. Comme vous le verrez, vous pouvez faire des dessins assez étonnants avec cette capacité simple.

Essayons quelques lignes de code Python pour créer une nouvelle tortue et commençons à dessiner une figure simple comme un rectangle. Nous ferons référence à notre première tortue en utilisant le nom de variable ``alex``, mais souvenez-vous que vous pouvez choisir le nom de votre choix aussi longtemps que vous suivez les règles de noms du chapitre précédent.

Le programme, tel qu’il est montré, ne dessinera que les deux premiers côtés du rectangle. Après la ligne 4, vous aurez une ligne droite allant du centre du dessin à la droite. Après la ligne 6, vous aurez une toile avec une tortue et un rectangle à moitié dessiné. Appuyez sur le bouton Exécuter pour essayer et voir.

Le programme, tel qu’il est montré, ne dessinera que les deux premiers côtés du rectangle. Après la ligne 4, vous aurez une ligne droite allant du centre du dessin à la droite. Après la ligne 6, vous aurez une toile avec une tortue et un rectangle à moitié dessiné. Appuyez sur le bouton Exécuter pour essayer et voir.

.. activecode:: turtle_intro_1
    :nocodelens:

    import turtle            	# nous permet d'utiliser la bibliothèque de *turtues*
    window = turtle.Screen()    # crée une fenêtre graphique
    alex = turtle.Turtle()   	# crée une tortue nommée alex
    alex.forward(150)        	# dit à alex d'avancer de 150 pas
    alex.left(90)           	# tourne de 90 degrés
    alex.forward(75)         	# complète le deuxième côté d'un rectangle qui mesure 75 pas


.. admonition:: **Essayez ceci!**

    Modifiez le programme ci-dessus en ajoutant les commandes nécessaires pour que *alex* complète le rectangle.


Comprendre un programme de *turtle*
-------------------------------------

Voici quelques points que vous devez comprendre sur le programme de *turtle* que nous avons écrit ci-dessus.

La première ligne indique à Python de chercher un **module** nommé ``turtle``. Ce module nous apporte deux nouveaux types que nous pouvons utiliser: le type ``Turtle`` et le type ``Screen``. La notation avec un point ``turtle.Turtle`` signifie *"Le type de *Turtle* défini dans le module turtle"*. (N'oubliez pas que Python est sensible à la casse, le nom du module, ``turtle``, avec un ``t`` minuscule, est différent du type ``Turtle`` en raison du ``T`` majuscule.)

Nous créons ensuite et ouvrons ce que le module turtle appelle un écran/*screen* (nous préférerions l'appeler une fenêtre ou, dans le cas de cette version Web de Python, simplement un toile), que nous affectons à la variable ``window``. Chaque fenêtre contient une **toile**, qui est la zone à l'intérieur de la fenêtre sur laquelle nous pouvons dessiner.

Dans la ligne 3, nous créons une tortue. La variable ``alex`` fait référence à cette tortue. Ces trois premières lignes nous préparent à dessiner.

Aux lignes 4 à 6, nous ordonnons à **l'objet** ``alex`` de se déplacer et de se tourner. Nous faisons cela en **invoquant** ou en activant les méthodes à **alex** - ce sont les instructions auxquelles toutes les tortues savent répondre. Ici, le point indique que les méthodes invoquées appartiennent à, et font référence à l'objet ``alex``.


**Vérifie ta compréhension**

.. mchoice:: turtle_intro_check_1
   :answer_a: Nord
   :answer_b: Sud
   :answer_c: Est 
   :answer_d: Ouest
   :correct: c
   :feedback_a: Certains systèmes de tortues commencent avec une tortue qui fait face au nord, mais pas celle-ci.
   :feedback_b: Non, regardez le premier exemple avec une tortue. Dans quelle direction se déplace la tortue?
   :feedback_c: Oui, la tortue commence face à l'est.
   :feedback_d: Non, regardez le premier exemple avec une tortue. Dans quelle direction se déplace la tortue?

   Dans quelle direction la tortue fait-elle face lorsqu'elle est créée?


Programmes mixtes
~~~~~~~~~~~~~~~~~~~~

.. parsonsprob:: turtle_intro_parsons_1

   Le programme suivant utilise une tortue pour dessiner un L majuscule, comme indiqué dans l’image, <img src="../../_static/parsons/TurtleL4.png" width="150" align="left" hspace="10" vspace="5" /> mais les lignes sont mélangées. Le programme doit faire tous les réglages nécessaires comme: importer le module turtle, obtenir la fenêtre sur laquelle on peut dessiner et créer la tortue. Rappelez-vous que la tortue commence face à l'est quand elle est créée. La tortue doit se tourner vers le sud et tracer une ligne de 150 pixels de long, puis se tourner vers l’est et tracer une ligne de 75 pixels de long. Nous avons ajouté une boussole à la photo pour indiquer les directions nord, sud, ouest et est. <br /><br /><p>Faites glisser les blocs d'instructions de la colonne de gauche vers la colonne de droite et placez-les dans le bon ordre. Cliquez ensuite sur <i>Check Me</i> pour voir si vous avez raison. On vous dira si des lignes sont dans le mauvais ordre.</p>
   
   -----
   import turtle
   window = turtle.Screen()
   ella = turtle.Turtle()
   =====
   ella.right(90)
   ella.forward(150)
   =====
   ella.left(90)
   ella.forward(75)


.. parsonsprob:: turtle_intro_parsons_2

   Le programme suivant utilise une tortue pour dessiner une coche comme indiqué à gauche, <img src="../../_static/parsons/TurtleCheckmark4.png" width="150" align="left" hspace="10" vspace="5" /> mais les lignes sont mélangées. Le programme doit faire tous les réglages nécessaires comme: importer le module turtle, obtenir la fenêtre sur laquelle on peut dessiner et créer la tortue. La tortue doit faire face au sud-est, tracer une ligne de 75 pixels de long, ensuite faire face au nord-est, et tracer une ligne de 150 pixels de long. Nous avons ajouté une boussole à la photo pour indiquer les directions nord, sud, ouest et est. Le nord-est est entre le nord et l'est. Le sud-est est entre le sud et l'est. <br /><br /><p>Faites glisser les blocs d'instructions de la colonne de gauche vers la colonne de droite et placez-les dans le bon ordre. Cliquez ensuite sur <i>Check Me</i> pour voir si vous avez raison. On vous dira si des lignes sont dans le mauvais ordre.</p>
   
   -----
   import turtle
   =====
   window = turtle.Screen()
   =====
   maria = turtle.Turtle()
   =====
   maria.right(45)
   maria.forward(75)
   =====
   maria.left(90)
   maria.forward(150)

.. parsonsprob:: turtle_intro_parsons_3

   Le programme suivant <img src="../../_static/parsons/TurtleLineToWest.png" width="150" align="left" hspace="10" vspace="5" /> utilise une tortue pour dessiner une ligne unique à l'ouest, comme indiqué à gauche, mais les lignes de programme sont mélangées. Le programme doit faire tous les réglages nécessaires comme: importer le module turtle, obtenir la fenêtre sur laquelle on peut dessiner et créer la tortue. La tortue doit alors se tourner pour faire face à l'ouest et tracer une ligne de 75 pixels de long. <br /><br /><p>Faites glisser les blocs d'instructions de la colonne de gauche vers la colonne de droite et placez-les dans le bon ordre. Cliquez ensuite sur <i>Check Me</i> pour voir si vous avez raison. On vous dira si des lignes sont dans le mauvais ordre.</p>

   -----
   import turtle
   window = turtle.Screen()
   jamal = turtle.Turtle()
   jamal.left(180)
   jamal.forward(75)

Les Méthodes de tortu/*Turtle Methods*
----------------------------------------

Un objet peut avoir différentes méthodes (choses qu'il peut faire), et il peut aussi avoir des **attributs** (parfois appelés *propriétés/properties*). Par exemple, chaque tortue a un attribut *color*. L’appel de la méthode ``alex.color ("red")`` fera qu'alex soit rouge et que la ligne qu'il dessine sera aussi rouge.

La couleur de la tortue, la largeur de son stylo (queue), la position de la tortue dans la fenêtre, son orientation, etc. font tous partie de son **état** actuel. De même, la fenêtre de l'objet a une couleur d'arrière-plan qui fait partie de son état.

Il existe un grand nombre de méthodes qui nous permettent de modifier les objets; tortue et fenêtre. Dans l'exemple ci-dessous, nous montrons simplement quelques une et n'avons commenté que les lignes qui diffèrent de l'exemple précédent. Notez également que nous avons décidé d'appeler notre objet tortue *tess* et avons changé le nom de l'objet Screen à *wn*.


.. activecode:: turtle_intro_2
    :nocodelens:
    
    import turtle

    wn = turtle.Screen()
    wn.bgcolor("lightgreen")        # définit la couleur de fond de la fenêtre color

    tess = turtle.Turtle()
    tess.color("blue")              # tess est bleu
    tess.pensize(3)                 # définit la largeur de son stylo

    tess.forward(50)
    tess.left(120)
    tess.forward(50)

    wn.exitonclick()                # attendez qu'un utilisateur clique sur la fenêtre pour fermer


La dernière ligne joue un rôle très important. La variable *wn* fait référence à la fenêtre ci-dessus. Lorsque nous appelons sa méthode ``exitonclick``, le programme suspend l'exécution et attend que l'utilisateur clique avec la souris quelque part dans la fenêtre. Lorsque cet événement click se produit, la réponse est de fermer la fenêtre graphique et de quitter (arrêter l'exécution du programme) Python.

Chaque fois que nous exécutons ce programme, une nouvelle fenêtre de dessin s’affiche et reste affichée jusqu’à ce que nous cliquions dessus.


Vérifie ta compréhension
-------------------------

.. mchoice:: turtle_intro_check_2
   :answer_a: Il crée un nouvel objet tortue pouvant être utilisé pour dessiner.
   :answer_b: Il définit le module tortue qui vous permettra de créer un objet Tortue et de dessiner avec lui.
   :answer_c: La tortue dessine la moitié d'un rectangle à l'écran.
   :answer_d: Rien, c'est inutile.
   :correct: b
   :feedback_a: La ligne &quotalex = turtle.Turtle()&quot est ce qui crée réellement l'objet tortue.
   :feedback_b: Cette ligne importe le module appelé tortue, qui possède toutes les fonctions intégrées pour dessiner à l'écran avec l'objet Tortue.
   :feedback_c: cette fonctionnalité est réalisée avec les lignes: &quotalex.forward(150)&quot, &quotlex.left(90)&quot, and &quotalex.forward(75)&quot
   :feedback_d: Si on ne le met pas dans le programme, Python donnera une erreur en disant qu'il ne connaît pas le nom &quotturtle&quot when it reaches the line &quotwn = turtle.Screen()&quot
   
   If we leave it out, Python will give an error saying that it does not know about the name &quotturtle&quot quand il atteint la ligne &quotwn = turtle.Screen()&quot

   Considérons le code suivant:

   .. code-block:: python

     import turtle
     wn = turtle.Screen()
     alex = turtle.Turtle()
     alex.forward(150)
     alex.left(90)
     alex.forward(75)

   Que fait la ligne "import turtle"?

.. mchoice:: turtle_intro_check_3
   :answer_a: Ceci est simplement pour plus de clarté. Il serait également utile de simplement taper "Turtle()" au lieu de "turtle.Turtle()".
   :answer_b: Le point (.) indique à Python que nous souhaitons appeler un nouvel objet.
   :answer_c: La première "tortue" (avant le point) indique à Python que nous faisons référence au module turtle, où se trouve l'objet "Turtle".
   :correct: c
   :feedback_a: Nous devons spécifier le nom du module où Python peut trouver l'objet Turtle.
   :feedback_b: Le point sépare le nom du module et le nom de l'objet. Les parenthèses à la fin sont ce qui dit à Python d’appeler un nouvel objet.
   :feedback_c: Oui, le type de tortue est défini dans le module turtle. Rappelez-vous que Python est sensible au majuscule et que **T**urtle est différente de **t**urtle.

   Pourquoi tapons-nous ``turtle.Turtle()`` pour obtenir un nouvel objet Turtle?


.. mchoice:: turtle_intro_check_4
   :answer_a: Vrai
   :answer_b: Faux
   :correct: a
   :feedback_a: Dans ce chapitre, vous avez vu une nommée alex et une nommée tess, mais tout nom de variable est autorisé.
   :feedback_b: une variable, y compris une qui fait référence à un objet Turtle, peut avoir le nom que vous choisissez, dans la mesure où elle respecte les conventions de dénomination du chapitre 2.

   Vrai ou Faux: un objet Tortue peut avoir n'importe quel nom qui suit les règles de nommage du Chapitre 2.

.. mchoice:: turtle_intro_check_5
   :answer_a: <img src="../../_static/parsons/test1Alt1.png" alt="right turn of 90 degrees before drawing, draw a line 150 pixels long, turn left 90, and draw a line 75 pixels long">
   :answer_b: <img src="../../_static/parsons/test1Alt2.png" alt="left turn of 180 degrees before drawing,  draw a line 150 pixels long, turn left 90, and draw a line 75 pixels long">
   :answer_c: <img src="../../_static/parsons/test1Alt3.png" alt="left turn of 270 degrees before drawing,  draw a line 150 pixels long, turn left 90, and draw a line 75 pixels long">
   :answer_d: <img src="../../_static/parsons/test1Alt4v2.png" alt="right turn of 270 degrees before drawing, draw a line 150 pixels long, turn right 90, and draw a line 75 pixels long">
   :answer_e: <img src="../../_static/parsons/test1correct.png" alt="left turn of 90 degrees before drawing,  draw a line 150 pixels long, turn left 90, and draw a line 75 pixels long">
   :correct: e
   :feedback_a: Ce code ferait tourner la tortue vers le sud avant de dessiner
   :feedback_b: Ce code ferait tourner la tortue vers l'ouest avant de dessiner
   :feedback_c: Ce code ferait tourner la tortue vers le sud avant de dessiner
   :feedback_d: Ce code est presque correct, mais l'extrémité courte serait tournée vers l'est plutôt que vers l'ouest.
   :feedback_e: Oui, la tortue commence en fesant face à l'est. Pour tourner au nord, vous pouvez tourner à gauche de 90 degrés ou à droite de 270 degrés.

   Lequel des codes suivants produirait l'image suivante? 

   .. image:: images/turtleTest1.png
      :alt: long line to north with shorter line to west on top
      :width: 150px

D'autres programmes mélangé/*More Mixed Up Programs!*
--------------------------------------------------------

.. parsonsprob:: turtle_intro_parsons_4

   Le programme suivant utilise une tortue pour dessiner un L majuscule en blanc sur un fond bleu, comme indiqué à gauche, <img src="../../_static/parsons/BlueTurtleL.png" width="150" align="left" hspace="10" vspace="5" /> mais les lignes sont mélangées. Le programme doit effectuer tous les réglages nécessaires comme: créer la tortue et définir la taille du stylo à 10, la tortue doit ensuite se tourner vers le sud, tracer une ligne de 150 pixels de long, se tourner vers l'est et trancer une ligne de 75 pixels de long. Enfin, définissez la fenêtre pour qu'elle se ferme lorsque l'utilisateur clique dessus. <br /><br /><p>Faites glisser les blocs d'instructions de la colonne de gauche vers la colonne de droite et placez-les dans le bon ordre. Cliquez ensuite sur <i>Check Me</i> pour voir si vous avez raison. On vous dira si des lignes sont dans le mauvais ordre.</p>

   -----
   import turtle
   wn = turtle.Screen()
   =====
   wn.bgcolor("blue")     	
   jamal = turtle.Turtle()
   =====
   jamal.color("white")               	
   jamal.pensize(10) 
   =====
   jamal.right(90)
   jamal.forward(150)
   =====
   jamal.left(90)
   jamal.forward(75)
   wn.exitonclick()

.. parsonsprob:: turtle_intro_parsons_5

   Le programme suivant utilise une tortue pour dessiner un T majuscule en blanc sur un fond vert comme indiqué à gauche, <img src="../../_static/parsons/TurtleT.png" width="150" align="left" hspace="10" vspace="5"/> mais les lignes sont mélangées. Le programme doit effectuer tous les réglages nécessaires comme: créer la tortue et définir la taille du stylo à 10. Après cela, la tortue doit se tourner vers le nord, tracer une ligne de 150 pixels de long, se tourner vers l'ouest et tracer une ligne de 50 pixels de long. Ensuite, la tortue devrait tourner à 180 degrés et tracer une ligne de 100 pixels de long. Enfin, définissez la fenêtre pour qu'elle se ferme lorsque l'utilisateur clique dessus. <br /><br /><p>Faites glisser les blocs d'instructions de la colonne de gauche vers la colonne de droite et placez-les dans le bon ordre. Cliquez ensuite sur <i>Check Me</i> pour voir si vous avez raison. On vous dira si des lignes sont dans le mauvais ordre.</p>

   -----
   import turtle
   wn = turtle.Screen()
   wn.bgcolor("green")     	
   jamal = turtle.Turtle()
   jamal.color("white")               	
   jamal.pensize(10) 
   =====
   jamal.left(90)
   jamal.forward(150)
   =====
   jamal.left(90)
   jamal.forward(50)
   =====
   jamal.right(180)
   jamal.forward(100)
   =====
   wn.exitonclick()


Problèmes de pratique
------------------------

Essayez les problèmes de pratique suivants. Vous pouvez travailler directement dans ce manuel ou utiliser Thonny. Dans tous les cas, veillez enregistrer votre solution dans votre dossier Infromatique 20 lorsque vous avez terminé!

La documentation Python du module tortue pourrait vous être utile: `https://docs.python.org/fr/3/library/turtle.html <https://docs.python.org/fr/3/library/turtle.html>`_ 

.. attention::

   Assurez-vous de NE PAS enregistrer un fichier sous le nom ``turtle.py``. Si vous le faites, lorsque vous appelez ``import turtle``, Python recherche un fichier appelé turtle.py, ce qui signifie qu'il importera le fichier turtle.py que vous venez de sauvegarder. Vous obtiendrez une erreur lors de la tentative de création d'un objet Screen() ou Turtle(), car ils ne seront pas définis.



Sélection de couleur
~~~~~~~~~~~~~~~~~~~~~~~~~

Modifiez le programme indiqué ci-dessous afin qu'avant de créer la fenêtre, il invite l'utilisateur à saisir la couleur d'arrière-plan souhaitée. Il convient de stocker la réponse de l'utilisateur dans une variable et de modifier la couleur de la fenêtre en fonction des souhaits de l'utilisateur. Effectuez des modifications similaires pour permettre à l'utilisateur de définir également la couleur de la tortue nommée Bree.

(Hint: vous pouvez trouver une liste des noms de couleurs autorisés à l'adresse suivante: `https://www.w3schools.com/colors/colors_names.asp <https://www.w3schools.com/colors/colors_names.asp>`_ . Ce site comprend des exemples assez inhabituels, comme "PeachPuff" et "HotPink".)


.. note:: 
    Si vous utilisez votre code dans Thonny, l'ordre de vos instructions est très important, car une fenêtre s'ouvrira devant la fenêtre principale de Thonny (alors que dans le navigateur, la fenêtre n'est qu'un canevas sur la page Web). Vous voudrez peut-être poser des questions à l'utilisateur *avant* de créer un Screen() sur lequel dessiner. Bien que vous puissiez utiliser quelque chose comme ``easygui_qt`` pour poser les questions avec des fenêtres contextuelles, il existe également une fonction ``screen.textinput ("Nom de la fenêtre", "Question à poser")`` intégrée au module tortue cela fera apparaître la question dans une fenêtre pop-up. Vous devez utiliser l'instance turtle.Screen() lors de l'appel de la fonction ``textinput``. Par exemple:: 
      
      canvas = turtle.Screen()
      question = canvas.textinput("Nom de la fenêtre", "Question à poser")

    Sachez cependant que la fonction ``textinput()`` ne fonctionnera pas dans la version de Python de ce navigateur.


.. activecode:: practice_problem_turtle_intro_1
    :nocodelens:
    :enabledownload:

    # Sélection de couleur

    import turtle

    # créer une fenêtre et définir sa couleur
    canvas = turtle.Screen()
    canvas.bgcolor("lightgreen")        

    # créer la tortue, et ses attributs
    bree = turtle.Turtle()
    bree.color("blue")
    bree.pensize(3)

    #dessiner!
    bree.forward(100)
    bree.right(60)
    bree.forward(100)

**Ne regardez pas** cet exemple de solution à moins que vous n'ayez déjà fini de créer votre propre solution!

.. reveal:: reveal_solution_practice_problem_turtle_intro_1
    :showtitle: Voir la Solution
    :hidetitle: Masquer la Solution

    La solution suivante fonctionnera bien dans le navigateur, où une zone de saisie de texte apparaît automatiquement lorsque vous appelez la fonction ``input()``::

      # Sélection de couleur

      import turtle

      # créer une fenêtre et définir sa couleur
      canvas = turtle.Screen()
      the_background_color = input("Veuillez entrer une couleur de l'arrière-plan:")
      canvas.bgcolor(the_background_color)

      # créer la tortue, et ses attributs
      bree = turtle.Turtle()
      brees_color = input("Veuillez entrer la couleur de la tortue:")
      bree.color(brees_color)
      bree.pensize(3)

      #dessiner!
      bree.forward(100)
      bree.right(60)
      bree.forward(100)

    Si vous utilisez Thonny pour créer votre solution, vous souhaiterez probablement utiliser la fonction ``screen.textinput("nom de la fenêtre", "question à poser")`` lors de la demande de saisie de l'utilisateur. Voici une version qui fait ça::

      # Sélection de couleur

      import turtle

      # créer une fenêtre et définir sa couleur
      canvas = turtle.Screen()
      the_background_color = canvas.textinput("Couleur", "Veuillez saisir une couleur d'arrière-plan: ")
      canvas.bgcolor(the_background_color)

      # créer la tortue, et ses attributs
      bree = turtle.Turtle()
      brees_color = canvas.textinput("Couleur", "Veuillez saisir la couleur de la tortue:")
      bree.color(brees_color)
      bree.pensize(3)

      #dessiner!
      bree.forward(100)
      bree.right(60)
      bree.forward(100)


Dessiner un carré de n'importe quelle taille
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Créez un programme qui utilise le module tortue pour dessiner un carré. L'utilisateur doit pouvoir définir un certain nombre d'options chaque fois que le code est exécuté. Le programme doit donc lui demander:

- la largeur du stylo de la tortue
- la couleur de la tortue
- la longueur des côtés du carré qui sera tracé
- la couleur de fond à utiliser
   
*Hint:* votre entrée de l'utilisateur retournera une chaîne, mais la méthode ``pensize`` des tortues s'attend à ce que son argument soit un ``int``. Cela signifie que vous devez convertir la chaîne en *int* avant de la passer à ``pensize``.

.. activecode:: practice_problem_turtle_intro_2
    :nocodelens:
    :enabledownload:

    # Que fait ce programme?
    # Mon nom
    # Date

    import turtle

    # Mon code

