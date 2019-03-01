.. qnum::
   :prefix: conditionals
   :start: 1


Conditionnelles
================

.. topic:: Aperçu rapide de la journée

    Révisez les problèmes de pratique du dernier jour. Donnez plus de détails sur les expressions booléennes. Pratiquez certains problèmes Python avec les entrées/sorties (*input/Renvoi/output*) et les conditions.


.. reveal:: curriculum_addressed_conditionals
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.


Que fait ce programme?
---------------------------

Rappelez-vous que dans notre aperçu rapide de Python, nous avons vu dans la section :ref:`math_operator_list` qu'un seul signe égal ``=`` est utilisé pour **assigner** une valeur. Deux signes égaux ``==`` sont utilisés pour **comparer** une valeur.

.. note:: Votre enseignant peut choisir d'utiliser les exemples suivants comme activité de classe, en les affichant et en vous demandant de deviner ce que chacun va faire avant d'exécuter le code.

Que vont produire les programmes suivants? Pourquoi?

.. activecode:: wdtpd_conditionals_1
    :caption: Que va imprimer ce programme?
    :nocodelens:

    nombre  = 20
    nombre  = nombre  + 10

    if nombre  == 10:
      print("La valeur 10 est affectée au numéro")

    if nombre  == 20:
      print("La valeur 20 est affectée au numéro")

    if nombre  == 30:
      print("La valeur 30 est affectée au numéro")


.. activecode:: wdtpd_conditionals_2
    :caption: Que va imprimer ce programme?
    :nocodelens:

    age = 15
    nom = "Zoe"

    if age == 15:
      print("Vous avez presque l'âge de conduire par vous-même.")
    else:
      print("Sois plus âgé sois moins âgé de 15 ans.")


.. activecode:: wdtpd_conditionals_3
    :caption: Que va imprimer ce programme?
    :nocodelens:

    age = 15
    nom = "Zoe"

    if age == 15:
      print("Vous avez presque l'âge de conduire par vous-même.")
    elif nom == "Zoe":
      print("Bonjour Zoe! Ravi de te voir!")
    else:
      print("Sois plus âgé sois moins âgé de 15 ans.")


.. activecode:: wdtpd_conditionals_4
    :caption: Que va imprimer ce programme?
    :nocodelens:

    age = 15
    nom = "Zoe"

    if nom == "Eli":
      print("Je suis content de vous revoir!")
    elif age == 16:
      print("Vous pouvez conduire!")
    else:
      print("Ca fait longtemps depuis notre dernière visite!")

    print("Je suis un peu fatigué.")


.. index:: booleans

Booléens/*booleans*
---------------------

Le type Python pour stocker les valeurs true et false est appelé ``bool``, nommé après le mathématicien britannique George Boole. George Boole a créé *L'Algèbre Booléennes*, qui est la base de toute arithmétique informatique moderne.

Il n'y a que deux **valeurs booléennes**. Ils sont ``True`` et ``False``. La capitalisation est importante, puisque ``true`` et ``false`` ne sont pas des valeurs booléennes (rappelez-vous que Python est sensible à la différence entre majuscule et minuscule).

.. note:: Les valeurs booléennes ne sont pas des chaînes!

    Il est extrêmement important de réaliser que True et False ne sont pas des chaînes. Ils ne sont pas entourés de guillemets. Ce sont les deux seules valeurs du type de données ``bool``. Examinez de près les types présentés ci-dessous.


.. activecode:: boolean_1
    :nocodelens:

    print(type(True))
    print(type("True"))

Une **expression booléenne** est une expression dont le résultat est une valeur booléenne. L'opérateur d'égalité, ``==``, compare deux valeurs et produit une valeur booléenne indiquant si les deux valeurs sont égales.

.. activecode:: boolean_2
    :nocodelens:

    print(5 == 5)
    print(5 == 6)

.. index:: comparison operators

Dans la première instruction, les deux opérandes sont égaux, ainsi l'expression est évaluée à ``True``. Dans la deuxième déclaration, 5 n'est pas égal à 6, nous obtenons donc ``False``.

L'opérateur ``==`` est l'un des six opérateurs de comparaison **comparison operators**; les autres sont:

.. sourcecode:: python

    x != y               # x n'est pas égal à y
    x > y                # x est supérieur à y
    x < y                # x est inférieur à y
    x >= y               # x est supérieur ou égal à y
    x <= y               # x est inférieur ou égal à y

Nous en avons déjà utilisé la plupart de ces dernier, mais ``!=`` Est nouveau pour nous. Vous devez également vous rappeler que nous avons utilisé ``not`` avec Reeborg et que ``not`` modifie la valeur d'une expression booléenne. Considérer ce qui suit:

.. activecode:: boolean_3
    :nocodelens:

    print(5 != 5)
    print(not 5 != 5)


Lorsqu'on demande à l'ordinateur une question avec une expression booléenne, une erreur courante consiste à utiliser un seul signe égal (``=``) au lieu d'un double signe égal (``==``). Rappelez-vous que ``=`` est un opérateur d'affectation et ``==`` est un opérateur de comparaison.



Problèmes de pratique
-------------------------

Essayez les problèmes de pratique suivants. Vous pouvez travailler directement dans ce manuel ou utiliser Thonny. Dans tous les cas, veillez enregistrer votre solution dans votre dossier Informatique 20 lorsque vous avez terminé!

.. note:: N'oubliez pas que chaque fois que vous prenez une entrée ``input()`` de l'utilisateur, le type de données de cette entrée sera une chaîne! Parfois, vous devez convertir ce que l'utilisateur entre en nombre.


Ajouter / Soustraire Deux nombres
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ecrivez un programme qui peut additionner ou soustraire deux nombres. Vous devez d’abord demander à l’utilisateur s’il souhaite ajouter ou soustraire, puis prendre les deux nombres, puis enfin effectuer l’opération requise et imprimer le résultat.


.. activecode:: practice_problem_conditionals_1
    :nocodelens:
    :enabledownload:

    # Ajouter/Soustraire Deux nombres
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici


**Ne regardez pas** cet exemple de solution à moins que vous n'ayez déjà fini de créer votre propre solution!

.. reveal:: reveal_solution_practice_problem_conditionals_1
    :showtitle: Voir solution possible
    :hidetitle: Masquer la solution possible

    C'est une solution possible. Notez que ce n'est pas particulièrement efficace, car le même code apparaît dans les blocs ``if`` et ``elif``. Cela peut être amélioré une fois la *scope* et les fonctions des variables soit comprises.::

      # Ajouter/Soustraire Deux nombres
      # Arman Gentil-Perret
      # le 30 jan, 2019

      operateur_choisi = input("Voulez-vous ajouter (+) ou soustraire (-)? ")

      if operateur_choisi == "+":
          #Cherche l'entré de l'utilisateur
          premier_numero  = input("Veuillez entrer le premier nombre : ")
          deuxieme_numero  = input("Veuillez entrer le deuxième nombre : ")

          #convertir l'entrée en nombres
          premier_numero  = float(premier_numero)
          deuxieme_numero  = float(deuxieme_numero)
          
          la_reponse = premier_numero + deuxieme_numero 
          print("La réponse quand vous ajoutez est", la_reponse)

      elif operateur_choisi == "subtract":
          #Cherche l'entré de l'utilisateur
          premier_numero  = input("Veuillez entrer le premier nombre : ")
          deuxieme_numero  = input("Veuillez entrer le deuxième nombre : ")

          #convertir l'entrée en nombres
          premier_numero  = float(premier_numero)
          deuxieme_numero  = float(deuxieme_numero)
          
          la_reponse = premier_numero - deuxieme_numero 
          print("La réponse lorsque vous soustrayez est", la_reponse)

      else:
          #ni "+" ni "-" a été entré 
          print("Erreur. Je ne sais pas ce que cela signifie. Veuillez entrer '+' ou '-'.")
        
        

Calculateur d'aire d'une surface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ecrivez un programme qui demande à l'utilisateur s'il souhaite trouver l'aire d'un rectangle, d'un cercle ou d'un triangle. Demandez ensuite à l'utilisateur de saisir les tailles appropriées (longueur et largeur, rayon ou base et hauteur) pour la forme à calculer. Enfin, effectuez le calcul et affichez le résultat avec un beau message. *Remarque: Vous voudrez peut-être utiliser le code que vous avez créé dans le programme Ajouter/Soustraire Deux nombres pour vous aider à créer des parties de ce code!*


.. activecode:: practice_problem_conditionals_2
    :nocodelens:
    :enabledownload:

    # Calculateur d'aire d'une surface
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici


Si vous avez des problèmes - Voici plus de détails sur les conditions
-------------------------------------------------------------------------------


``if/else``
~~~~~~~~~~~~

Les structures de contrôle ``if``, ``if/else`` et ``if/elif/else`` sont toutes appelées des instructions conditionnelles/*conditional statements*. Notez que chaque fois que vous posez une question à l'ordinateur à l'aide de l'une de ces instructions conditionnelles, Python l'évalue comme une expression booléenne.

.. activecode:: conditionals_1
    :nocodelens:

    x = 15

    if x % 2 == 0:
        print(x, "est pair")
    else:
        print(x, "est impair")

.. sidebar::  Organigramme d'une instruction **if** avec un **else**

   .. image:: images/flowchart_if_else.png

Comme avec Reeborg, la syntaxe d'une instruction ``if`` ressemble à ceci:

.. sourcecode:: python

    if EXPRESSION BOOLÉENNE:
        INSTRUCTION_1        # exécutée si la condition est évaluée à True
    else:
        INSTRUCTION_2        # exécuté si la condition est évaluée à False

L'expression booléenne après l'instruction ``if`` est appelée **condition**. Si c'est le cas, les instructions qui suit qui sont indentée en tabulation sont exécutées. Si non, les instructions indentées sous la clause ``else`` sont exécutées.

Les instructions indentée qui suivent l'instruction ``if`` sont appelées un **bloc**. Il n'y a pas de limite au nombre d'instructions pouvant apparaître sous les deux clauses d'une instruction ``if``, mais il doit y avoir au moins une instruction dans chaque bloc.


.. mchoice:: conditionals_mc_1
   :answer_a: TRUE
   :answer_b: FALSE
   :answer_c: sur une ligne et FALSE sur la suivante
   :answer_d: rien ne sera imprimé
   :correct: b
   :feedback_a: TRUE est imprimé par le bloc if, qui ne s’exécute que si le conditionnel (dans ce cas, 4 + 5 == 10) est vrai. Dans ce cas, 5 + 4 n'est pas égal à 10.
   :feedback_b: Puisque 4 + 5 == 10 est évalué à False, Python ignorera le bloc if et exécutera l'instruction du bloc else.
   :feedback_c: Python n'imprimera jamais les valeurs TRUE et FALSE car il n'exécutera seulement un des blocs if ou else, mais pas les deux.
   :feedback_d: Python exécutera toujours soit le bloc if (si la condition est vraie), soit le bloc else (si la condition est fausse). Il ne sauterait jamais les deux blocs.

   Qu'est-ce que le code suivant imprime (choisissez parmi la sortie a, b, c ou rien)?

   .. code-block:: python

     if 4 + 5 == 10:
         print("TRUE")
     else:
         print("FALSE")


.. mchoice:: conditionals_mc_2
   :answer_a: Renvoi/Renvoi/output a
   :answer_b: Renvoi/Renvoi/output b
   :answer_c: Renvoi/Renvoi/output c
   :answer_d: Renvoi/Renvoi/output d
   :correct: c
   :feedback_a: Bien que TRUE soit imprimé une fois l'instruction if-else terminée, les deux blocs de l'instruction if-else impriment également quelque chose. Dans ce cas, Python aurait dû ignorer les deux blocs de l'instruction if-else, ce qu'il ne ferait jamais.
   :feedback_b: Comme il y a un TRUE imprimé après la fin de l'instruction if-else, Python imprimera toujours TRUE comme dernière instruction.
   :feedback_c: Python imprimera FALSE à partir du bloc else (car 5 + 4 n’est pas égal à 10), puis affichera TRUE à la fin de l'instruction if-else
   :feedback_d: Pour imprimer ces trois lignes, Python devrait exécuter les deux blocs de l'instruction if-else, ce qu'il ne peut jamais faire.

   Qu'est-ce que le code suivant imprime?

   .. code-block:: python

     if 4 + 5 == 10:
         print("TRUE")
     else:
         print("FALSE")
     print("TRUE")

   ::

      a. TRUE

      b.
         TRUE
         FALSE

      c.
         FALSE
         TRUE
      d.
         TRUE
         FALSE
         TRUE


``if``
~~~~~~~

.. sidebar::  Organigramme d'un **if** sans **else**

   .. image:: images/flowchart_if_only.png

Une autre forme de l’instruction ``if`` est celle dans laquelle la clause ``else`` est entièrement omise. Cela crée ce qu'on appelle parfois **sélection unaire/unary selection**. Dans ce cas, lorsque la condition est évaluée à ``True``, les instructions sont exécutées. Sinon, le flux/*flow* d'exécution continue avec l'instruction après le corps du ``if``.


.. activecode:: conditionals_if_1
    :nocodelens:

    x = 10
    if x < 0:
        print("Le nombre négatif  ",  x, " n'est pas valide ici.")
    print("Ceci est toujours imprimé")


Que serait imprimé si la valeur de ``x`` est négative? Essayez-le


**Check your understanding**

.. mchoice:: conditionals_if_mc_1
   :answer_a: Renvoi/output a
   :answer_b: Renvoi/output b
   :answer_c: Renvoi/output c
   :answer_d: Cela provoquera une erreur car chaque *if* doit avoir une clause *else*.
   :correct: b
   :feedback_a: Puisque -10 est inférieur à 0, Python exécutera le corps de l'instruction *if* ici.
   :feedback_b: Python exécute le corps du bloc if ainsi que l’instruction qui suit le bloc *if*.
   :feedback_c: Python exécutera également l'instruction qui suit le bloc if (car elle n'est pas incluse dans un bloc else, mais plutôt une instruction normale).
   :feedback_d: Il est valide d'avoir un bloc *if* sans bloc *else* correspondant (mais vous ne puissiez pas avoir un bloc *else* sans un bloc *if* correspondant).


   Qu'est-ce que le code suivant imprime?

   .. code-block:: python
     
     x = -10
     if x < 0:
         print("Le nombre négatif  ",  x, " n'est pas valide ici.")
     print("Ceci est toujours imprimé")

   ::

     a.
     Ceci est toujours imprimé

     b.
     Le nombre négatif  -10 n'est pas valide ici
     Ceci est toujours imprimé

     c.
     Le nombre négatif  -10 n'est pas valide ici


``if/elif/else``
~~~~~~~~~~~~~~~~~

``elif`` est une abréviation de ``else if``. Rappelez-vous que seulement une branche sera exécutée. Il n'y a pas de limite au nombre d'instructions ``elif`` mais seulement une instruction unique (et facultative) finale ``else`` est autorisée et il sera la dernière branche de l'instruction.

.. image:: images/flowchart_chained_conditional.png

Chaque condition est vérifiée en ordre. Si le premier est faux, le suivant est vérifié, et ainsi de suite. Si l'une d'entre elles est vraie, la branche correspondante est exécutée et l'instruction se termine. **Même si plusieurs conditions sont vraies, seule la première branche vraie est exécutée**.


.. activecode:: conditionals_if_elif_else_1
    :nocodelens:
    
    x = 10
    y = 10

    if x < y:
        print("x est inférieur à y")
    elif x > y:
        print("x est supérieur à y")
    else:
        print("x et y doivent être égaux")