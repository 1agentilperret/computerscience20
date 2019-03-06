.. qnum::
   :prefix: intro-string-operators
   :start: 1


Opérateur de chaînes et temps de travail
==========================================

.. topic:: Aperçu rapide de la journée

    Découvrez comment les opérateurs ``+`` et ``*`` fonctionnent avec les chaînes. Continuez à travailler sur le premier projet Python, axée sur les entrées/sorties, les types de données et les conditions.


.. reveal:: curriculum_addressed_intro_string_operators
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.


Que fait ce programme?
---------------------------

Comme vous l'avez vu dans les questions WDTPD de la dernière leçon, l'utilisation de l'opérateur "*" avec des chaînes donne un résultat très différent de l'utilisation de l'opérateur "*" avec des données numériques. Réfléchissez attentivement aux questions suivantes, en vous assurant de bien comprendre POURQUOI ils affichent ce qu’ils affichent.

.. note:: Votre enseignant peut choisir d'utiliser les exemples suivants comme activité de classe, en les affichant et en vous demandant de deviner ce que chacun fera avant d'exécuter le code.

**Que vont produire les programmes suivants? Pourquoi??**

Qu'est-ce que cela va imprimer si vous entrez ``15``? Pourquoi ne pas taper ``hey`` pour voir ce qui va imprimer? 

.. activecode:: wdtpd_string_operators_1
    :caption: Que va imprimer ce programme?
    :nocodelens:

    nombre = input("Quelle valeur devrions-nous changer? ")
    valeur_changee = nombre * 4
    print(valeur_changee)

Entrez ``3`` et ``5`` lorsque vous exécutez le code ci-dessous. Que va imprimer le programme? *Indice: ce ne sera pas une erreur!*


.. activecode:: wdtpd_string_operators_2
    :caption: Que va imprimer ce programme?
    :nocodelens:

    premier_nombre = input("Veuillez entrer le premier numéro: ")
    deuxieme_nombre = input("Veuillez entrer le deuxième numéro: ")
    valeur_combinee = premier_nombre + deuxieme_nombre
    print(valeur_combinee)

Tapez votre prénom et votre nom de famille lorsque vous exécutez le code ci-dessous. Comment pouvez-vous corriger ce code pour écrire votre nom correctement?

.. activecode:: wdtpd_string_operators_3
    :caption: Corrige la sortie de ce code.
    :nocodelens:

    prenom = input("Veuillez entrer votre prénom: ")
    nom = input("Veuillez entrer votre nom de famille: ")
    nom_complet = prenom + last_nom
    print("Je suis content de vous rencontrer" + nom_complet)


.. index:: concatenation

Opérations avec les chaînes
-----------------------------

En général, vous ne pouvez pas effectuer d’opérations mathématiques sur des chaînes, même si les chaînes ressemblent à des nombres. Les actions suivantes sont interdis (en supposant que ``message`` a une chaîne de caractères comme valeur):

.. sourcecode:: python
    
    message - 1   
    "Bonjour" / 123   
    message * "Bonjour"   
    "15" + 2

Fait intéressant, l’opérateur ``+`` fonctionne avec des chaînes, mais pour les chaînes, l’opérateur ``+`` représente **la concaténation/l'enchainement**, pas l’addition. La concaténation signifie joindre les deux opérandes en les reliant bout à bout. C'est l'équivalent d'utiliser le bloc de Scratch regrouper |scratch_join_block_inline|. Par exemple:

.. |scratch_join_block_inline| image:: images/scratch_join_block.png

.. activecode:: string_concatenation
    :nocanvas:

    fruit = " banane"
    pateCuit = "pain aux noix "
    print(pateCuit + "et à la" + fruit)

Le résultat de ce programme est ``pain aux noix et à la banane``. Les espaces à la fin du mot ``noix`` et au début du mot ``banane`` font partie de la chaîne et sont nécessaires pour produire l'espace entre les chaînes concaténées. Sortez les espaces et exécutez-le à nouveau.

L'opérateur "*" fonctionne également sur les chaînes. Il effectue une répétition. Par exemple, ``"fun"*3`` est ``"FunFunFun"``. L'un des opérandes doit être une chaîne et l'autre doit être un entier.


.. activecode:: string_repetition
    :nocanvas:

    print("Go" * 6)

    nom = "Blades"
    print(nom * 3)

    print(nom + "Go" * 3)

    print((nom + "Go") * 3)

Cette interprétation de ``+`` et ``*`` est logique par analogie avec l'addition et la multiplication. Tout comme ``4 * 3`` est équivalent à ``4 + 4 + 4``, nous nous attendons à ce que ``"Go" * 3`` soit identique à ``"Go"+"Go"+"Go"``, et c'est vrais dans ce cas. Notez également dans le dernier exemple que l'ordre des opérations pour ``*`` et ``+`` est le même que pour l'arithmétique (PEDMAS). La répétition est faite avant la concaténation. Si vous voulez que la concaténation soit faite en premier, vous devez utiliser une parenthèse.


Vérifie ta compréhension
----------------------------

.. mchoice:: string_operators_practice_1
   :answer_a: python rocks
   :answer_b: python
   :answer_c: pythonrocks
   :answer_d: Erreur, vous ne pouvez pas ajouter deux chaînes ensemble.
   :correct: c
   :feedback_a: La concaténation n'ajoute pas automatiquement d'espace.
   :feedback_b: l'expression chaine_un + chaine_deux est évaluée en premier, puis la chaîne résultante est imprimée
   :feedback_c: Oui, les deux chaînes sont collées bout à bout.
   :feedback_d: L'opérateur "+" a différentes significations selon les opérandes, dans ce cas, nous avons deux chaînes.

   Qu'est-ce qui est imprimé par les déclarations suivantes?
   
   .. code-block:: python

      chaine_un = "python"
      chaine_deux = "rocks"
      print(chaine_un + chaine_deux)



.. mchoice:: string_operators_practice_2
   :answer_a: python!!!
   :answer_b: python!python!python!
   :answer_c: pythonpythonpython!
   :answer_d: Erreur, vous ne pouvez pas effectuer de concaténation et de répétition en même temps.
   :correct: a
   :feedback_a: Oui, la répétition a priorité sur la concaténation.
   :feedback_b: La répétition est faite en premier.
   :feedback_c: L'opérateur de répétition affect la variable *exclamation*.
   :feedback_d: Les opérateurs "+" et "*" sont définis pour les chaînes ainsi que pour les nombres.


   Qu'est-ce qui est imprimé par les déclarations suivantes?
   
   .. code-block:: python
 
      chaine_un = "python"
      exclamation = "!"
      print(chaine_un + exclamation * 3)


Temps de travail
---------------------

Veuillez passer le reste de la classe à continuer le travail sur votre projet Python (probablement un projet d'entrée/sortie). Si vous avez complètement terminé cette tâche, vous voudrez peut-être regarder vers la prochaine tâche ou demander à votre enseignant quels autres défis vous pouvez relever.