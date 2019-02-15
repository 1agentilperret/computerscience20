.. qnum::
   :prefix: quick-overview
   :start: 1



Aperçu rapide de Python
=========================

.. note:: Dans l'exploration rapide de Python, vous verrez certaines choses que vous ne comprenez pas. Cela est bien et ne vous inquiétez pas. Nous aborderons chacune des idées de manière beaucoup plus détaillée au fur et à mesure que le semestre avance, mais il est vraiment utile de voir un aperçu général avant d'entrer dans les détails de chaque section.

Si vous préférez regarder cette `vidéo <https://www.youtube.com/watch?v=d97kS830e-c>`_ décrivant certaines fonctionnalités importantes de Python.

.. youtube:: d97kS830e-c
    :height: 315
    :width: 560
    :align: left
    :http: https


Qu'est ce que Python?
----------------------

Python est un langâge de programmation qui vous permet d’apprendre à l’ordinateur à faire ce que vous voulez. Vous avez déjà écrit des programmes Python avec Reeborg. Tout ce que vous avez déjà appris (à l'exception de `repeat`) fonctionne en Python normal. L’utilisation régulière de Python nous permet de commencer à explorer d’autres manières dont nos programmes peuvent produire des sorties et prendre des entrées.

.. index:: Thonny

Exécuter Python sur votre ordinateur
---------------------------------------

Il existe de nombreuses façons d’installer Python sur votre ordinateur (en fait, une version de Python est peut-être déjà installée sur votre ordinateur). Cependant, l’un des moyens les plus simples de faire fonctionner Python sur votre ordinateur (Windows, Mac ou Linux) consiste à `download Thonny <http://thonny.org/>`_. Allez télécharger Thonny maintenant. L'installation ne nécessite pas de droits d'administrateur. Vous devriez donc pouvoir l'installer dans le laboratoire informatique de votre école (vérifiez bien auprès de votre enseignant qu'il accepte cette tâche en premier!). Vous voudrez peut-être également installer Thonny à la maison.

Pour chacun des segments de code que vous voyez sur cette pâge, vous pouvez les exécuter directement dans votre navigateur Web **OU** vous pouvez copier/coller le code dans **Thonny** pour l'exécuter.

Lorsque vous utilisez Thonny, vous devez comprendre la différence entre l'éditeur **de texte** et le **shell** (également appelé l'interprèteur/*interpreter*). Si vous souhaitez enregistrer votre code pour l'utiliser ultérieurement, vous devez le saisir dans l'éditeur de texte, ce qui vous invitera à enregistrer votre fichier quelque part sur le disque lorsque vous appuierez sur le bouton Exécuter (*ou sur F5*). La sortie de votre code apparaîtra dans le shell (sous l'éditeur de texte). Vous pouvez également saisir le code Python de votre choix dans le shell, ce qui constitue un moyen pratique d'essayer de nouvelles choses en Python.

.. imâge:: imâges/thonny_window.png


.. index:: whitespace, syntax error

Espace blanc/*Whitespace*
--------------------------

Comme lors de la programmation de Reeborg, il est très important **d'indenter votre code correctement** en Python. Par exemple, le code ci-dessous provoquera une **erreur de syntaxe** lorsque vous cliquerez sur le bouton Exécuter. Cliquez sur le bouton Exécuter pour voir l'erreur. Maintenant, pouvez-vous comprendre comment résoudre ce problème? Modifiez le code, puis cliquez à nouveau sur Exécuter pour voir si vous l'avez corrigé!


.. activecode:: syntax_error_indentation
    :caption: corrige l'erreur de syntaxe en mettant correctement le code en retrait.
    :nocodelens:

    un_nombre = 5
    if un_nombre > 3:
    print("Oui, le nombre est plus grand.")

.. index:: print

Impression de données sorties/*Printing Output*
--------------------------------------------------

Comme vous l'avez vu dans l'exemple ci-dessus, vous pouvez ``print()`` /*imprimer* des choses sur la sortie standard (généralement la console/interpréteur Python). La fonction ``print()`` sera utilisée dans beaucoup des exemples suivants. Notez que ``print()`` peut prendre autant d'arguments qu'on veut, séparés par des virgules. Ainsi, vous pouvez imprimer quelque chose comme ceci: ``print ("lundi", "mardi", "mercredi")``, qui afficherait ``lundi mardi mercredi``, chaque argument étant séparé par un espace.

.. note:: Il y a beaucoup d'autres façons pour un programme de produire une sortie, comme dessiner, allumer des LED, etc. Nous étudierons certaines de celles-ci plus tard dans le cours.

.. index:: variables, data types

Variables et types de données/*Variables and Data Types*
----------------------------------------------------------------

Espérons que vous vous souveniez d’utiliser des variables pour garder une trace des choses lorsque nous utilisions Scratch. Par exemple, nous avons utilisé une variable appelée «nombre de côtés» lorsque nous avons commencé à dessiner des polygones réguliers. En Python, nous pouvons également créer des variables. Dans l'exemple ci-dessus, nous avons créé une variable appelée `un_numbre`. Nous devons faire attention à la façon dont nous nommons les variables, car elles ne peuvent pas être des mots-clés tels que `if`,`not`, etc. Un mot-clé est un mot qui a déjà une signification spéciale en Python. Les variables doivent commencer par une lettre et si elles contiennent plus d'un mot, vous devez mettre un trait de soulignement entre les mots (comme `variable_utile` ou `quelque_chose_d_autre`).

Les types de données fondamentaux qui nous préoccupent en Python incluent:

- **int** (entier/*integer*, tel que ``3`` ou ``-5``)
- **float** (nombre à virgule flottante/*floating point nombre*, tel que ``1.2`` ou ``-4.75``)
- **str** (chaîne/*string*, telle que ``"hello"`` ou ``'Friday'`` or ``"5"``)
- **bool** (booléen/*boolean*, telle que ``True`` ou ``False``)

Nous utiliserons chacun des types de données indiqués ci-dessus tout au long du cours, et il est **vraiment important** que vous compreniez les différences qui existent entre eux. Prenez un moment pour répondre aux questions suivantes.

**Vérifie ta compréhension**

.. mchoice:: data_types_1_1
    :answer_a: booléen
    :answer_b: nombre
    :answer_c: float
    :answer_d: chaîne
    :correct: d
    :feedback_a: Ce n'est pas ``True`` ou ``False``.
    :feedback_b: Les données ne sont pas numériques.
    :feedback_c: La valeur n'est pas numérique avec un point décimal.
    :feedback_d: Génial! Les chaînes sont toujours entre guillemets.

    Quel est le type de données de ``"c'est quel type de données"``?

.. mchoice:: data_types_1_2
    :answer_a: booléen
    :answer_b: nombre
    :answer_c: float
    :answer_d: chaîne
    :correct: b
    :feedback_a: Ce n'est pas ``True`` ou ``False``.
    :feedback_b: Génial! Les données sont numériques, sans point décimal.
    :feedback_c: La valeur n'est pas numérique avec un point décimal.
    :feedback_d: Les chaînes sont **toujours** entre guillemets.

    Quel est le type de données de ``3``?

.. mchoice:: data_types_1_3
    :answer_a: booléen
    :answer_b: nombre
    :answer_c: float
    :answer_d: chaîne
    :correct: a
    :feedback_a: Génial! Le booléen est ``True`` ou ``False``.
    :feedback_b: Les données ne sont pas numériques.
    :feedback_c: La valeur n'est pas numérique avec un point décimal.
    :feedback_d: Les chaînes sont **toujours** entre guillemets.

    Quel est le type de données de ``True``?

.. mchoice:: data_types_1_4
    :answer_a: booléen
    :answer_b: nombre
    :answer_c: float
    :answer_d: chaîne
    :correct: c
    :feedback_a: Ce n'est pas ``True`` ou ``False``.
    :feedback_b: Les données ne sont pas numériques.
    :feedback_c: Génial! La valeur est numérique avec un point décimal.
    :feedback_d: Les chaînes sont **toujours** entre guillemets.

    Quel est le type de données de ``1.5``?


Vérifier les types de données
-------------------------------

Si vous n'êtes pas sûr du type de données, vous pouvez le vérifier en utilisant la fonction ``type()``. Cela fonctionne à la fois sur les valeurs (un élément de données) et sur les variables (un contenant qui contient une valeur). Que fera le code ci-dessous? Après avoir appuyé sur Exécuter ci-dessous, modifiez la valeur dans la fonction ``type()`` pour vous assurer que vous comprenez vraiment ce qu'elle fait. Remplacez le ``5`` par le ``5.3``. Qu'est ce que tu obtiens? Que serait le résultat si on le change à ``"5.3"``?


.. activecode:: checking_data_types
    :nocodelens:

    print(type(5))


.. index:: type casting

.. _type_casting_functions:

Conversion des types de données
------------------------------------

Parfois, vous devrez peut-être convertir un type de données en un autre. Vous pouvez utiliser les fonctions suivantes pour **type cast**/**saisir** des données:

- ``str(x)`` pour convertir **x** en chaîne
- ``int(x)`` pour convertir **x** en nombre
- ``float(x)`` pour convertir **x** en nombre à virgule flottante

.. activecode:: casting_data_types
    :nocodelens:

    a = 4         #a est un int
    print( type(a) )

    b = str(a)    #b devient la chaîne de a: '4'
    print( type(b) )

    c = float(b)  #c devient le float de a: 4.0
    print( type(c) )


.. index:: math operators

.. _math_operator_list:

Opérateurs mathématiques
--------------------------

Nous pouvons faire des calculs avec Python, mais nous devons connaître les opérateurs à utiliser. Le tableau suivant démontre les opérateurs mathématiques les plus fréquemment utilisés dans Python.

=========   ==============================    ===============       ======
Symboles    Operations                        Example               Sortie
=========   ==============================    ===============       ======
\+          Addition                          ``1 + 2``             3
\-          Soustraction                      ``2 - 1``             1
\*          Multiplication                    ``2 * 2``             4
/           Division                          ``5 / 2``             2.5
//          Division Tronquée (quotient)      ``5 // 2``            2
%           Modulo (reste)                    ``5 % 2``             1
\*\*        Puissance                         ``5 ** 2``            25
=========   ==============================    ===============       ======


.. index:: if


``if`` - ``si``
----------------

La structure de contrôle ``if`` fonctionne comme elle le faisait avec Reeborg. Exécutez l'exemple donné ci-dessous. Que se passe-t-il si vous le changez à ``nombre = 23``. Et si vous le changez à ``nombre = 10``?

.. note:: Un seul signe égal ``=`` est utilisé pour **assigner** une valeur. Deux signes égaux ``==`` sont utilisés pour **comparer** une valeur.

.. activecode:: if_intro_1
    :nocodelens:

    nombre = 900

    if nombre == 900:
        print("Freddy Krueger est au téléphone.")

    if nombre == 23:
        print("Michael Jordan est le GOAT (Greatest of All Time)")


.. index:: if-elif-else

``if/elif/else`` - *si/alors/sinon*
-------------------------------------

La structure de contrôle ``if/elif/else`` fonctionne exactement de la même manière que lors de la programmation de Reeborg. La chose importante à retenir est que **seulement une des branches peut exécuter**. Lisez le code ci-dessous et prédisez ce que vous pensez sera la sortie. Puis changez-le en ``température = 25``. Quelle sera la sortie maintenant? Et si vous le changiez en ``température = 5``? Ensuite ``température = 15``?

.. activecode:: if_elif_else_intro
    :nocodelens:

    température = -3

    if température < -10:
        print("porter une manteau d'hiver")
    elif température < 15:
        print("porter une chemise à manches longues")
    else:
        print("porter un t-shirt")


.. index:: while

Boucle ``while`` *loop*
-----------------------------------

Rappelez-vous que nous avons utilisé une boucle ``while`` dans Reeborg quand on ne connaît pas le nombre d’itérations à l’avance. En d'autres termes, le *corps* de while sera répété tant que l'expression booléenne de contrôle renvois ``True``. Exécutez le code ci-dessous. Pouvez-vous changer le code pour qu'il **compte** de 1 à 10 au lieu de compter à rebour de 10, puis indique "J'arrive!"?


.. activecode:: while_loop_intro
    :nocodelens:

    conteur = 10

    while conteur > 0:
        print(conteur)
        conteur = conteur - 1   #diminue le compteur à chaque itération

    print("Blastoff!")


.. index:: for

boucle ``for`` *loop*
-----------------------

Lorsque nous avons connu le nombre exact d'itérations nécessaires dans Reeborg, nous avons utilisé la commande ``repeat``. Cette commande ne faisait pas partie de la norme Python. Elle a été ajoutée pour que le codâge de Reeborg soit aussi simple que possible. Bien que je n’explique pas encore tous les détails à ce sujet, je vais vous présenter la version Python d’une boucle de répétition ``for``. Si nous voulons que quelque chose se répète 10 fois, nous pourrions faire ce qui suit: (après avoir exécuté le code, changez le ``10`` en un autre nombre et essayez à nouveau)


.. activecode:: for_loop_intro_1
    :nocodelens:

    for conteur in range(10):
        print(conteur)

Notez que la boucle ci-dessus se répète 10 fois, mais commence à compter depuis 0. Le dernier nombre est donc un 9. Nous pouvons contrôler la boucle ``for`` encore plus en passant entre deux arguments, comme ceci:

.. activecode:: for_loop_intro_2
    :nocodelens:

    for conteur in range(5, 11):
        print(conteur)


.. index:: lists

Des listes
------------

Comment fonctionne le **range** ci-dessus? Cela crée une **liste** de nombres, ce qui nous permet d’enregistrer plus d’une valeur dans la même variable. Par exemple, lorsque nous avons appelé ``range(5, 11)`` ci-dessus, Python a créé une liste avec les nombres 5, 6, 7, 8, 9, 10. Si nous avions voulu créer cette liste nous-mêmes, nous aurions pu fait quelque chose comme ça:

.. code-block:: python

    liste_de_nombres = [5, 6, 7, 8, 9, 10]

Nous pouvons insérer n'importe quel type de données dans une liste, il serait donc possible de créer une liste comme celle-ci:

.. code-block:: python

    liste_de_nombres = [5, "heureux", 2.5, True]

Si nous créons notre propre liste, nous pouvons toujours y parcourir à l'aide d'une boucle ``for``. Par exemple, si vous tenez comptes des achats que vous vouliez chercher au magasin, vous pourriez mettre tous les articles que vous voulez acheter dans une liste, puis les *imprimer*/*print*.

.. activecode:: list_intro_3
    :nocodelens:

    liste_epiceries = ["des pommes", "des carottes", "du lait", "du yogourt"]
    for article in liste_epiceries:
        print("N'oubliez pas d'acheter", article)

Si vous souhaitez accéder à un seul élément dans une liste, vous pouvez spécifier l'emplacement de l'élément souhaité. Par exemple, si nous voulions accéder aux *carottes* de la liste d'épicerie ci-dessus, nous pourrions demander le 1er élément (puisque nous commençons à compter à partir de 0). Nous plaçons l'emplacement entre crochets/*brackets*. Pour accéder aux carottes, nous appellerions ``liste_epiceries[1]``.

.. activecode:: list_intro_4
    :nocodelens:

    liste_epiceries = ["des pommes", "des carottes", "du lait", "du yogourt"]
    print("N'oubliez pas d'acheter", liste_epiceries[1])


.. index:: functions

Les fonctions
--------------

Tout comme vous avez pu apprendre à Reeborg à faire de nouvelles choses en créant une nouvelle fonction, nous pouvons également créer de nouvelles fonctions en Python. Voici quelques exemples:

.. activecode:: functions_overview_intro_1
    :nocodelens:

    def dit_bonjour():
        print("Bonjour!")

    dit_bonjour()


.. activecode:: functions_overview_intro_2
    :nocodelens:

    def dit_bonjour(un_nom):
        print("Bonjour,", un_nom)

    dit_bonjour("Jérémie")


.. index:: input

Saisir des données de l'utilisateur/*Taking Input from User*
---------------------------------------------------------------------

Si vous voulez que l'utilisateur tape quelque chose, vous pouvez utiliser la fonction ``input()``. Voici quelques exemples:

.. note:: ``input()`` retournera toujours une **chaîne**. Vous devrez le convertir en **int** ou **float** si vous voulez un nombre.


.. activecode:: input_intro_1
    :nocodelens:

    ton_nom = input("Quel est votre nom?")
    print(ton_nom)


.. activecode:: input_intro_2
    :nocodelens:

    def dit_bonjour(un_nom):
        print("Bonjour, ", un_nom)

    ton_nom = input("Quel est votre nom?")
    dit_bonjour(ton_nom)

L'exemple suivant ne fonctionnera pas lorsque vous essayez de l'exécuter. Essayez d'entrer ``16``, puis ``15``. Notez que rien n’est imprimé, même s’il semble que le conditionnel devrait l’imprimer. Pouvez-vous comprendre ce qui ne va pas et le réparer? **Astuce: pensez aux types de données!**

.. activecode:: input_intro_3
    :nocodelens:
    :caption: Pouvez-vous comprendre ce qui ne va pas?

    âge = input("Quel âge avez-vous?")

    if âge == 16:
        print("Vous pouvez obtenir votre permis de conduire!")
    elif âge == 15:
        print("Vous pouvez obtenir votre permis de conduire d'apprenti.")


.. index:: import

Modules Python
---------------

Un des avantages de Python est qu’il existe de nombreux modules qui augmanter les fonctionnalités de base de Python. Un module est simplement un fichier (ou dossier) contenant des fonctions et des variables Python. Vous avez créé votre propre module lorsque vous exploriez Reeborg. Lorsque vous avez tapé ``from library import *``, vous avez mis toutes les fonctions de l'onglet Library à la disposition de votre programme. Veuillez noter que bien que nous puissions utiliser la syntaxe ``from library import *``, cela peut poser problème si vous créez accidentellement une fonction portant le même nom que quelque chose que vous avez importé. Voir le deuxième exemple ci-dessous pour la méthode d'importation recommandée.

.. activecode:: module_intro_1
    :nocodelens:
    :caption: Cela fonctionne, mais n'est pas recommandé.

    from math import *

    print( sqrt(16) )
    print( cos(0) )

.. activecode:: module_intro_2
    :nocodelens:
    :caption: C’est le meilleur moyen d’importer un module.

    import math

    print( math.sqrt(16) )
    print( math.cos(0) )

.. activecode:: module_intro_3
    :nocodelens:

    import random

    print( random.randrange(1, 10) )


Jeu de devinettes de nombre
-----------------------------

Rappelez-vous le jeu de devinettes que nous avons créé dans Scratch? Le principe de base était le suivant:

- génère un nombre aléatoire de 1 à 100 et le garder dans une variable
- répète ce qui suit jusqu'à ce que l'utilisateur devine le nombre
- oblige l'utilisateur à deviner le nombre (en utilisant le bloc **demander__et attendre**)
- indique à l'utilisateur si le nombre est trop élevé ou trop bas
- félicite l’utilisateur quand il trouve le nombre exact avec un message du type "Bravo! Vous avez deviné le nombre exact en 9 essais!"

Nous allons essayer d'implémenter ce jeu en Python. **Remarque: vous rencontrerez probablement de nombreux problèmes lors de la création de ce jeu en Python.** Toutefois, il peut être très utile d’essayer des problèmes qui donnent l’impression d’être supérieurs à votre niveau. Bientôt, vous pourrez créer vous-même des programmes comme celui-ci! Votre enseignant peut choisir de vous donner un peu de temps pour essayer cela par vous-même, puis de démontrer une solution possible au problème, ou peut-être de revenir à ce jeu dans quelques semaines.


.. activecode:: nombre_guessing_game_attempératuret
    :caption: Créez un jeu de devinettes ici!

    
    # l'algorithme du jeu peut être décrit comme suit
    # votre travail consiste à essayer de convertir les commentaires en vrai code Python!

    # demande à l’ordinateur de choisir un nombre aléatoire compris entre 1 et 100


    # crée une variable pour suivre le nombre de suppositions prises


    # définit une variable avec une valeur initiale pour les utilisateurs, comme ceci: 
    # devinette_utilisateur = -1

    # répéter ce qui suit jusqu'à ce que l'utilisateur devine correctement

        # demander à l'utilisateur de deviner


        # met à jour la variable devinette_utilisateur


        # si ils devinent haut, dites-leur


        # si ils devinent bas, dites-leur


    # félicite l'utilisateur en lui disant combien de chance il lui a fallu pour deviner