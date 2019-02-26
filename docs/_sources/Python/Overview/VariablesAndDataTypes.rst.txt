.. qnum::
   :prefix: python-variables
   :start: 1


Variables, types de données et entrée par utilisateur
=======================================================

.. topic:: Aperçu rapide de la journée

    Donnez plus de détails sur les **variables**. Renforcer l'idée de **types de données**. Pratiquez certains problèmes de Python avec des **entrées/sorties** simples.


.. reveal:: curriculum_addressed_python_variables
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.


Que fait ce programme?
---------------------------

N'oubliez pas que nous avons appris quatre types de données de base dans notre vue d'ensemble de Python. Elles sont:

- ``int``
- ``float``
- ``string``
- ``bool``


.. note:: Votre enseignant peut choisir d'utiliser les exemples suivants comme activité de classe, en les affichant et en vous demandant de deviner ce que chacun va faire avant d'exécuter le code.

Pour les exemples suivants, considérons le type de données de chaque variable. Quelle sera la sortie du programme? Pourquoi?


.. activecode:: wdtpd_variable_assignment_1
    :caption: Que va imprimer ce programme?
    :nocodelens:

    x = 4
    y = 3 + x
    print(x + y)

.. activecode:: wdtpd_variable_assignment_3
    :caption: Que va imprimer ce programme?
    :nocodelens:

    x = 4
    y = 3
    z = "cinq"
    x = 2
    print(x + y)

.. activecode:: wdtpd_variable_assignment_2
    :caption: Que va imprimer ce programme?
    :nocodelens:

    x = 4
    y = 3
    z = "cinq"
    print(y + z)


Comment utiliser Thonny
-------------------------
 
Thonny peut être utilisé de deux manières: en *mode shell* et en *mode programme*. En mode shell, vous tapez des expressions Python dans le **shell de Python**, et l'interprèteur montre immédiatement le résultat. L'exemple ci-dessous montre le shell de Python en utilisation.

.. image:: images/thonny_shell.png

Le ``>>>`` est appelé **Python prompt** qui est l'interprète qui indique à l'utilisateur qu'il est prêt à recevoir des instructions. Nous avons tapé ``2 + 3``, puis appuyé sur **Entrée**. L'interprète a évalué notre expression et a répondu ``5``. À la ligne suivante il a donné une nouvelle invitation indiquant qu'il est prêt à recevoir plus d'*entrées*.

Travailler directement dans l’interprète est pratique pour tester de courts morceaux de code parce que vous obtenez une rétroaction immédiate. Voyez-le comme un papier brouillon qui vous aide à résoudre vos problèmes.

Alternativement, vous pouvez écrire un programme entier en plaçant des lignes d'instructions Python dans un fichier, ensuite utiliser l'interprète pour exécuter le contenu du fichier dans son ensemble. Un tel fichier est souvent appelé **code source**. Par exemple, nous avons utilisé Thonny pour créer un fichier de code source nommé ``firstprogram.py`` avec le contenu suivant:

.. image:: images/thonny_editor.png

Par convention, les fichiers contenant des programmes Python ont un nom qui se termine par ``.py``. Thonny enregistre automatiquement vos fichiers avec une extension .py. Vous devriez pouvoir les ouvrir dans Thonny en double-cliquant dessus dans l'explorateur de fichiers (ou dans Finder pour mac).

.. note:: Notez que lorsque nous utilisions le **shell**, nous n'avions pas à nous soucier d'utiliser ``print ()`` pour voir la valeur d'une instruction. Le shell le fait automatiquement. Cependant, si nous utilisons **l'éditeur de code**, nous devons appeler **print ()** à chaque fois que nous voulons afficher le résultat.

**Vérifie ta compréhension**

.. mchoice:: source_code_check
   :answer_a: les instructions d'un programme, enregistré dans un fichier.
   :answer_b:  le langage que vous utilisez pour programmer (ie: Python).
   :answer_c: l'environnement/l'outil dans lequel vous programmez.
   :answer_d: le numéro (ou "code") que vous devez entrer en haut de chaque programme pour indiquer à l'ordinateur comment exécuter votre programme
   :correct: a
   :feedback_a: Le fichier contenant les instructions écrites dans le langage évolué s'appelle le fichier de code source.
   :feedback_b: Ce langage s'appelle le langage de programmation ou simplement le langage.
   :feedback_c: L'environnement peut être appelé IDE ou environnement de développement intégré, mais pas toujours.
   :feedback_d: Il n’existe pas un numéro de ce type que vous devez taper au début de votre programme.

   Le code source est un autre nom pour:

.. index:: comments

Commentaires
--------------

À mesure que les programmes deviennent plus grands et plus compliqués, ils deviennent plus difficiles à lire. Les langages formels (ie: les langages de programmation) sont denses et il est souvent difficile de regarder un morceau de code et de comprendre ce qu'il fait ou pourquoi. Pour cette raison, il est judicieux d’ajouter des notes à vos programmes pour expliquer en langage naturel ce qu’il fait. Ces notes s'appellent des commentaires.

Un **commentaire** dans un programme informatique est un texte destiné uniquement au lecteur humain. Il est complètement ignoré par l'interprète. En Python, le jeton ``#`` commence un commentaire. Le reste de la ligne est ignoré. **Chaque programme que vous écrivez devrait commencer par un en-tête de commentaire**, qui pourrait ressembler à ceci:

.. activecode:: comment_header_example

    #---------------------------------------------------
    # Premier programme Python
    # Arman Gentil-Perret
    # le 20 jan, 2019
    #---------------------------------------------------

    print("Bonjour tout le monde!")


.. note:: Créez un dossier (appelez-le Informatique 20) sur votre ordinateur pour contenir tout le code que vous écrirez en Python ce semestre. Enregistrez le fichier que vous avez créé ci-dessus en tant que ``template.py`` et enregistrez-le dans ce dossier.

Notez que lorsque vous exécutez ce programme, il n’affiche que la phrase Bonjour tout le monde! Aucun des commentaires n'apparaissent. Vous remarquerez également que nous avons laissé une ligne vide dans le programme. Les lignes vides sont également ignorées par l'interprète, mais les commentaires et les lignes vides peuvent rendre vos programmes beaucoup plus faciles à analyser. Utilisez-les généreusement!


**Vérifie ta compréhension**

.. mchoice:: comment_check
   :answer_a: Pour dire à l’ordinateur ce que vous voulez dire dans votre programme.
   :answer_b: Pour que les personnes qui lisent votre code sachent, en langage naturel, ce que fait le programme.
   :answer_c: Rien, ce sont des informations superflues qui ne sont pas nécessaires.
   :answer_d: Rien dans un programme court. Ils ne sont nécessaires que pour les très gros programmes.
   :correct: b
   :feedback_a: Les commentaires sont ignorés par l'ordinateur.
   :feedback_b: L'ordinateur ignore les commentaires. C'est pour les humains qui "utiliser" votre programme.
   :feedback_c:  Les commentaires peuvent fournir des informations indispensables à la personne qui lit le programme.
   :feedback_d: Même les petits programmes bénéficient de commentaires.

   A quoi servent les commentaires?


.. index:: variables

Variables
---------

L'une des fonctionnalités les plus puissantes d'un langage de programmation est la possibilité de manipuler des **variables**. Une variable est un nom qui fait référence à une valeur.

**Les instructions d'affectation**/**Assignment statements** créent de nouvelles variables et leur donnent également des valeurs auxquelles se référer.

.. sourcecode:: python

    message = "Quoi de neuf, Doc?"
    n = 17
    pi = 3.14159

Cet exemple fait trois affectations. La première attribue la valeur d'une **chaîne** ``"Quoi de neuf, Doc?"`` À une nouvelle variable nommée `` message``. La seconde donne l'**entier** ``17`` à ``n`` et la troisième assigne le nombre à **virgule flottante** ``3.14159`` à une variable appelée ``pi``.

Le jeton **d'affectation**, ``=``, ne doit pas être confondu avec *égalité* (nous verrons plus tard que l'égalité utilise le jeton ``==``). La déclaration d'affectation lie un *nom*, à la gauche de ``=`` avec une *valeur*. C'est pourquoi vous obtiendrez une erreur si vous entrez:


.. sourcecode:: python

    17 = n

.. tip::

   Lorsque vous lisez ou écrivez du code, dites-vous que "n est affecté à 17" ou "n obtient la valeur 17" ou "n est une référence à l'objet 17" ou "n correspond à l'objet 17". Ne dites pas "n est égal à 17".

Une manière courante de représenter des variables sur du papier consiste à écrire le nom avec une flèche pointant vers la valeur de la variable. Ce type de figure, appelé **diagramme de référence**, est souvent appelé un **instantané d'état**/**state snapshot** car il indique l'état dans lequel se trouve chacune des variables à un instant donné. (Pensez-y comme à l'état d'esprit de la variable). Ce diagramme montre le résultat de l'exécution des instructions d'affectation présentées ci-dessus.

.. image:: images/refdiagram1.png
   :alt: Reference Diagram

Si vous demandez à Python d'évaluer une variable, cela produira la valeur qui est actuellement liée à la variable. En d'autres termes, l'évaluation d'une variable vous donnera la valeur à laquelle cette variable se réfère.


.. activecode:: variables_example_1
    :nocanvas:

    message = "Quoi de neuf, Doc?"
    n = 17
    pi = 3.14159

    print(message)
    print(n)
    print(pi)

Dans chaque cas, le résultat est la valeur de la variable.

Les variables ont aussi des types; encore une fois, nous pouvons demander à l'interprète ce qu'ils sont.

.. activecode:: variables_example_2
    :nocanvas:

    message = "Quoi de neuf, Doc?"
    n = 17
    pi = 3.14159

    print(type(message))
    print(type(n))
    print(type(pi))


Le type d'une variable est le type de l'objet auquel elle fait présentement référence.

Nous utilisons des variables dans un programme pour "mémoriser" des choses, comme le pointage actuel au match de basket. Mais les variables sont *variable*. Cela signifie qu'ils peuvent changer avec le temps, tout comme le tableau d'affichage d'un match de basket. Vous pouvez affecter une valeur à une variable, puis affecter une valeur différente à la même variable.
 
.. note::

    Ceci est différent des mathématiques. En maths, si vous donnez ``x`` la valeur 3, il ne peut pas changer pour faire référence à une valeur différente en plein milieu de vos calculs!    

Pour voir cela, lisez et ensuite exécutez le programme suivant. Vous remarquerez que nous modifions la valeur de ``journée`` trois fois, et lors de la troisième affectation, nous lui attribuons une valeur d'un type différent.

.. codelens:: variables_example_3
    :showoutput:

    journée = "Jeudi"
    print(journée)
    journée = "Vendredi"
    print(journée)
    journée = 21
    print(journée)


**Vérifie ta compréhension**

.. mchoice:: variables_check_1
   :answer_a: Rien n'est imprimé. Une erreur d'exécution se produit.
   :answer_b: Jeudi
   :answer_c: 32.5
   :answer_d: 19
   :correct: d
   :feedback_a: Il est possible de changer le type de données qu'une variable détient en Python.
   :feedback_b: Ceci est la première valeur attribuée à la variable journée, mais les instructions suivantes réaffectent cette variable à de nouvelles valeurs.
   :feedback_c: Il s'agit de la deuxième valeur attribuée à la variable journée, mais l'instruction suivante réaffecte cette variable à une nouvelle valeur.
   :feedback_d: La variable journée représentera la dernière valeur qui lui est assignée lors de son impression.
   
   Qu'est-ce qui est imprimé lorsque les instructions suivantes sont exécutées?

   .. code-block:: python

     journée = "Jeudi"
     journée = 32.5
     journée = 19
     print(journée)


.. index:: variable names

Noms de variables et mots-clés
-------------------------------

**Les noms de variables** peuvent être arbitrairement longs. Ils peuvent contenir à la fois des lettres et des chiffres, mais ils doivent commencer par une lettre ou un trait de soulignement. Vous devez utiliser des noms de variable descriptifs et possiblement longs. Par exemple, si vous créez un programme pour calculer la quantité d’essence consommée par une voiture, un bon nom de variable pourrait être ``litres_par_100_kms``. Un mauvais nom de variable dans ce cas serait ``l``. Utiliser une seule lettre comme nom de variable rend généralement votre programme plus difficile à comprendre pour les autres. Bien que cela puisse être un peu ennuyeux de taper un nom de variable long la première fois, une fois que vous l'avez tapé une fois dans Thonny, vous devriez pouvoir taper simplement les premières lettres du nom de la variable, puis appuyer sur **Ctrl-Espace** pour que le reste du nom de variable soit rempli automatiquement pour vous. *Si cela ne fonctionne pas pour vous, vérifiez les préférences de Thonny.*

Le trait de soulignement (``_``) peut également apparaître dans un nom. Il est souvent utilisé dans les noms avec plusieurs mots, tels que ``mon_nom`` ou ``prix_du_caffee_en_chine``. **C'est le moyen préféré d'écrire des noms de variables longs en Python, et vous devriez utiliser ce style!**

.. attention::

   Les noms de variables ne peuvent jamais contenir d'espaces.

Il existe certaines situations dans lesquelles les noms commençant par un trait de soulignement ont une signification particulière. Il est donc recommandé aux débutants de commencer par une lettre.

Bien qu'il soit possible d'utiliser des majuscules, par convention, nous ne le faisons pas. Si vous choisissez d'utiliser des lettres majuscules, rappelez-vous que majuscule et minuscule sont différents. ``Bruce`` et ``bruce`` sont des variables différentes.

.. note:: Les conventions concernant les noms de variable diffèrent d'une langue à l'autre. Un autre modèle d’appellation de variable courant consiste à utiliser une lettre minuscule pour le premier mot et à mettre en majuscule la lettre de départ de chaque mot qui suit. Par exemple, vous pouvez utiliser ``monNom`` ou ``prixDuCaffeeEnChine``. Ceci est souvent appelé camelCaps (pensez aux bosses d'un chameau).

Si vous attribuez un nom *illégal* à une variable, vous obtenez une erreur de syntaxe. Dans l'exemple ci-dessous, les noms de variable sont illégaux.

::

    76trombones = "grande parade"
    plus$ = 1000000
    class = "Informatique 101"


``76trombones`` est illégal car il ne commence pas par une lettre. "plus$" est illégal car il contient un caractère illégal, le signe de dollar. Mais qu'est-ce qui ne va pas avec ``class``?

.. index:: Python keywords

En effet, ``class`` est l’un des **mots-clés** de Python. Les mots-clés définissent les règles de syntaxe et la structure du langage. Ils ne peuvent pas être utilisés en tant que noms de variables. Python a une trentaine de mots-clés (et de temps en temps, des améliorations de Python introduisent ou éliminent un ou deux):

======== ======== ======== ======== ======== ========
and      as       assert   break    class    continue
def      del      elif     else     except   exec
finally  for      from     global   if       import
in       is       lambda   nonlocal not      or
pass     raise    return   try      while    with
yield    True     False    None
======== ======== ======== ======== ======== ========

Vous voudrez probablement garder cette liste à portée de main. Si l'interprète se plaint de l'un de vos noms de variable et que vous ne savez pas pourquoi, vérifier s'il se trouve dans cette liste.

**Les programmeurs choisissent généralement des noms pour leurs variables qui ont un sens pour les lecteurs humains du programme - ils aident le programmeur à documenter, ou à se rappeler, à quoi sert la variable.**


Entrée de l'utilisateur
-------------------------

Si vous voulez que l'utilisateur tape quelque chose, vous pouvez utiliser la fonction ``input()``. ``input()`` **retournera toujours une chaîne**. Vous devrez le convertir en **int** ou **float** si vous attendez un nombre.

.. activecode:: input_demo_1
    :nocodelens:
    
    ton_ecole = input("Quelle école fréquentez-vous?")
    print(ton_ecole)

L'exemple suivant ne fonctionnera pas lorsque vous essayez de l'exécuter. Pouvez-vous comprendre ce qui ne va pas et le réparer? *Conceil: pensez aux types de données!*

.. activecode:: input_demo_2
    :nocodelens:
    
    annee_presente = input("Quelle est l'année en cours?")
    annee_diplome = input("Quelle année obtiendrez-vous votre diplôme d'études secondaires?")

    annee_difference = annee_diplome - annee_presente

    print("Vous obtiendrez votre diplôme en", annee_difference, "ans.")

**Ne regardez pas** à la solution possible suivante jusqu'à ce qu vous avez passé du temps à essayer de créer votre propre solution!

.. reveal:: reveal_solution_input_demo_2
    :showtitle: Voir Solution
    :hidetitle: Masquer Solution

    Voici une solution possible::

        annee_presente = input("Quelle est l'année en cours?")
        annee_diplome = input("Quelle année obtiendrez-vous votre diplôme d'études secondaires?")

        # convertir les entrées utilisateur en entiers, afin que nous puissions soustraire
        annee_presente = int(annee_presente)
        annee_diplome = int(annee_diplome)

        annee_difference = annee_diplome - annee_presente

        print("Vous obtiendrez votre diplôme en", annee_difference, "ans.")



Problèmes de pratique
-----------------------

Essayez les problèmes de pratique suivants. Assurez-vous de savoir comment résoudre le problème avec du papier et un crayon avant d’essayer d’écrire une solution en Python! Vous pouvez travailler directement dans le manuel ou utiliser Thonny. Dans tous les cas, veillez **enregistrer votre solution** dans votre dossier Informatique 20 lorsque vous avez terminé!

.. note:: N'oubliez pas que chaque fois que vous prenez ``input()`` de l'utilisateur, le type de données de cette entrée sera une chaîne! Vous voudrez peut-être revenir sur :ref:`type_casting_functions`.


Aire de surface d'un cercle
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ecrivez un programme qui calculera l'aire d'un cercle. Invitez l'utilisateur à entrer le rayon. Imprimer un beau message pour présenter à l'utilisateur la réponse.

 
.. activecode:: practice_problem_variables_data_types_1
    :nocodelens:
    :enabledownload:

    # Calculateur de l'aire de la surface de cercle
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici

**Ne regardez pas** à la solution possible suivante jusqu'à ce qu vous avez déjà fini de créer votre propre solution!

.. reveal:: reveal_solution_practice_problem_variables_data_types_1
    :showtitle: Voir Solution
    :hidetitle: Masquer Solution

    Voici une solution possible::

        # Calculateur de l'aire de la surface de cercle
        # Arman Gentil-Perret
        # le 22 janvier, 2019

        pi = 3.14

        radius = input("S'il vous plaît entrer le rayon du cercle: ")
        radius = float(radius)  # convertir l'entrée en un nombre

        aire = pi*radius**2

        print("L'aire du cercle est", aire)



aire d'un rectangle
~~~~~~~~~~~~~~~~~~~~~~

Ecrivez un programme qui calculera l'aire d'un rectangle. Invitez l'utilisateur à inscrire la largeur et la hauteur du rectangle. Imprimer un beau message pour présenter à l'utilisateur la réponse.
   
.. activecode:: practice_problem_variables_data_types_2
    :nocodelens:
    :enabledownload:

    # Calculateur de l'aire de la surface d'un rectangle
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici


**Ne regardez pas** à la solution possible suivante jusqu'à ce qu vous avez déjà fini de créer votre propre solution!

.. reveal:: reveal_solution_practice_problem_variables_data_types_2
    :showtitle: Voir Solution
    :hidetitle: Masquer Solution

    Voici une solution possible::

        # Calculateur de l'aire de la surface d'un rectangle
        # Arman Gentil-Perret
        # le 23 janvier, 2019

        longeur = input("Entrez la longueur du rectangle: ")
        largeur = input("Entrez la largeur du rectangle: ")

        # convertir l'entrée utilisateur en nombres
        longeur = float(longeur)
        largeur = float(largeur)

        aire = longeur * largeur
        print("L'aire du rectangle est", aire)



Consommation de gaz de voiture
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ecrivez un programme qui calculera les litres par kilomètre (l/100km) utilisés par une voiture. Invitez l'utilisateur à entrer le nombre de kilomètres parcourus et le nombre de litres utilisés. Imprimez un beau message avec la réponse en litres/100km. *Remarque: si vous ne savez pas comment calculer L/100km, vous devriez essayer de le calculer à la main avant d'écrire un programme. Pour vous aider à vérifier votre travail, si vous avez parcouru 500km et utilisé 35L d’essence, vous devez obtenir 7L/100km*.


.. activecode:: practice_problem_variables_data_types_3
    :nocodelens:
    :enabledownload:

    # Calculateur kilométrage
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici


**Ne regardez pas** à la solution possible suivante jusqu'à ce qu vous avez déjà fini de créer votre propre solution!

.. reveal:: reveal_solution_practice_problem_variables_data_types_3
    :showtitle: Voir Solution
    :hidetitle: Masquer Solution

    Voici une solution possible::

        # Calculateur kilométrage
        # Arman Gentil-Perret
        # le 22 janvier, 2019

        kilometres_conduit = input("How many kilometers did you drive? ")
        litres_utilise = input("Combien de kilometres avez-vous parcourues? ")

        # convertir l'entrée utilisateur en nombres
        kilometres_conduit = float(kilometres_conduit)
        litres_utilise = float(litres_utilise)

        consommation_gas = litres_utilise / kilometres_conduit * 100

        print("Votre voiture utilise", consommation_gas, "L/100km")


Si vous finissez tôt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Si vous avez répondu à toutes les questions ci-dessus avant la fin du cours, essayez l'un des défis supplémentaires suivants:

- faire une calculatrice pour un problème mathématique plus compliqué.
- Vous regardez l'horloge et il est exactement 14 heures. Vous configurez une alarme pour qu'elle se déclenche dans 51 heures. À quelle heure l'alarme se déclenche? Ecrivez un programme Python pour résoudre la version générale de ce problème. Demandez à l'utilisateur l'heure actuelle (en heures) et demandez le nombre d'heures d'attente. Votre programme doit indiquer l’heure à laquelle le réveil se déclenche. Note: Vous voudrez peut-être revenir en arrière sur: :ref:`math_operator_list`.

