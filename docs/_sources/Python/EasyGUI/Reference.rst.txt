.. qnum::
   :prefix: easygui-reference
   :start: 1


.. _easygui_reference:

EasyGUI_Qt Référence
=======================

EasyGUI_Qt est inspiré de EasyGUI et contient un certain nombre de composants d'interface utilisateur graphiques de base. La version que vous utilisez est fournie à partir de `https://github.com/aroberge/easygui_qt <https://github.com/aroberge/easygui_qt>`_, et ajoute juste quelques modifications pour simplifier l'utilisation du logiciel (amélioration du processus d’installation en ajoutant PyQt5 comme dépendance, ajout de la fonction get_file_Nom). La référence suivante couvre un sous-ensemble des fonctions les plus accessibles pour un étudiant au niveau Info20. Vous pouvez donc consulter les `documents officiels du projet original <http://easygui-qt.readthedocs.io/en/ latest / api.html>`_ si vous souhaitez explorer davantage les options d’utilisation. Si vous explorez la documentation officielle, vous trouverez peut-être utile de savoir que vous pouvez appeler des fonctions avec seulement certains arguments (cela s'appelle des arguments facultatifs). Si vous faites cela, cependant, vous devrez spécifier *l'argument* que vous passez, comme ``easy.get_string (message = "Un prompt/une question:", réponse_par_défaut = "Une chaîne")``.


Installation
-------------

Dans Thonny, ouvrez Tools -> Manage Packages and type in ``cs20-easygui`` dans la barre de recherche, puis cliquez sur Installer. Cette installation prendra un certain temps car elle fait partie du moteur de rendu graphique principal (PyQt5).

Affichage des messages
----------------------------

Si vous appelez ``show_message`` avec un seul argument, cet argument devrait être une chaîne contenant le message que vous souhaitez afficher.


.. sourcecode:: python
    
    import easygui_qt as easy
    easy.show_message("Entrez votre message ici ou transmettez une variable contenant une chaîne.")

.. image:: images/showing-messages1.png

**Options additionelles**

Si vous appelez ``show_message`` avec un deuxième argument (séparé par une virgule), ce deuxième argument doit également être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy
    easy.show_message("Mon message est ici!", "Un titre")

.. image:: images/showing-messages2.png

Obtenir des chaînes
--------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à entrer une chaîne, utilisez la fonction ``get_string``. Cette fonction renverra ce que l'utilisateur saisira (sous forme de chaîne). Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``None``.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_string("Quel est votre nom?")

.. image:: images/getting-strings1.png

**Options additionelles**

Si vous appelez ``get_string`` avec un second argument (séparé par une virgule), ce second argument doit également être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_string("Quel est votre nom?", "Nom")

.. image:: images/getting-strings2.png

Si vous appelez ``get_string`` avec un troisième argument (séparé par une virgule), ce troisième argument doit également être une chaîne et sera interprété comme la valeur par défaut dans la zone de saisie.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_string("Quel est votre nom?", "Nom", "John Doe")

.. image:: images/getting-strings3.png


Obtenir des entiers/*intigers*
---------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à entrer un entier, utilisez la fonction ``get_integer``. Cette fonction renverra un entier et obligera l'utilisateur à ne saisir que des nombres. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``Aucun``.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_integer("Quel âge avez-vous?")

.. image:: images/getting-integers1.png


**Options additionelles**

Si vous appelez ``get_integer`` avec un deuxième argument (séparé par une virgule), ce dernier argument doit être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_integer("Quel âge avez-vous?", "Âge")

.. image:: images/getting-integers2.png

Si vous appelez ``get_integer`` avec un troisième argument (séparé par une virgule), ce troisième argument doit être un entier et sera interprété comme la valeur par défaut dans la zone de saisie.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_integer("Quel âge avez-vous?", "Age", 16)

.. image:: images/getting-integers3.png

Si vous appelez ``get_integer`` avec cinq arguments (séparés par des virgules), le quatrième argument doit être un entier représentant la valeur minimale autorisée, et le cinquième argument doit être un entier représentant la valeur maximale autorisée.


.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_integer("Quel âge avez-vous?", "Âge", 16, 0, 120)

.. image:: images/getting-integers4.png


Obtenir des virgules flotantes/*Floats*
-----------------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à entrer un float, utilisez la fonction ``get_float``. Cette fonction retournera un float et obligera l'utilisateur à entrer uniquement des valeurs numériques. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``Aucun``.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_float("Quelle est votre taille (en mètres)?")

.. image:: images/getting-floats1.png


**Options additionelles**

Si vous appelez ``get_float`` avec un deuxième argument (séparé par une virgule), ce dernier argument doit être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_float("Quelle est votre taille (en mètres)?", "Grandeur")

.. image:: images/getting-floats2.png

Si vous appelez ``get_float`` avec un troisième argument (séparé par une virgule), ce troisième argument doit être un float et sera interprété comme la valeur par défaut dans la zone de saisie.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_float("Quelle est votre taille (en mètres)?", "Grandeur", 1.82)

.. image:: images/getting-floats3.png

Si vous appelez ``get_float`` avec cinq arguments (séparés par des virgules), le quatrième argument doit être un nombre (int ou float) représentant la valeur minimale autorisée, et le cinquième argument doit être un nombre (int ou float) représentant le valeur maximale autorisée.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_float("Quelle est votre taille (en mètres)?", "Grandeur", 1.82, 0.22, 2.72)

.. image:: images/getting-floats4.png

Si vous appelez ``get_float`` avec six arguments (séparés par des virgules), le sixième argument doit être un entier représentant le nombre de décimales autorisées.

.. sourcecode:: python
    
    import easygui_qt as easy
    reponse = easy.get_float("Quelle est votre taille (en mètres)?", "Grandeur", 1.82, 0.22, 2.72, 2)

.. image:: images/getting-floats5.png

Obtenir une sélection d'une liste déroulante
-----------------------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à sélectionner une option dans une liste déroulante, utilisez la fonction ``get_choice``. Cette fonction renverra une chaîne contenant le choix de l'utilisateur. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``Aucun``.

Cette fonction nécessite trois arguments, le message d'invite/*prompt* (sous forme de chaîne), le titre de la fenêtre (sous forme de chaîne) et les choix que l'utilisateur peut choisir (sous forme de liste).


.. sourcecode:: python
    
    import easygui_qt as easy
    prompt = "Quel est votre sujet préféré?"
    titre = "Meilleur sujet"
    choix = ["Informatique", "Math", "Ed Phys", "Anglais", "Histoire"]

    reponse = easy.get_choice(prompt, titre, choix)

.. image:: images/getting-choice.png

Obtenir plusieurs sélections d'une liste
-------------------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à sélectionner une option (ou plusieurs options) dans une liste, utilisez la fonction ``get_list_of_choices``. Cette fonction renverra une liste contenant les choix de l'utilisateur. Si l'utilisateur appuie sur *Annuler*, ferme la fenêtre ou ne sélectionne aucune option, cette fonction renvoie une liste vide.

Cette fonction nécessite deux arguments, le titre de la fenêtre (sous forme de chaîne) et les choix que l'utilisateur peut choisir (sous forme de liste).

.. sourcecode:: python
    
    import easygui_qt as easy
    prompt = "Sujets que vous aimez"
    choix = ["Informatique", "Math", "Ed Phys", "Anglais", "Histoire"]

    reponse = easy.get_list_of_choices(prompt, choix)

.. image:: images/getting-multiple-selections.png

Obtenir un mot de passe
------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à entrer un mot de passe, utilisez la fonction ``get_password``. Cette fonction renverra une chaîne contenant la saisie de l'utilisateur. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``None``.

.. sourcecode:: python
    
    import easygui_qt as easy

    reponse = easy.get_password("Veuillez entrer votre mot de passe")

.. image:: images/getting-password1.png

**Options additionelles**

Si vous appelez ``get_password`` avec un deuxième argument (séparé par une virgule), ce dernier argument doit être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy

    reponse = easy.get_password("Veuillez entrer votre mot de passe", "Mot De Passe")

.. image:: images/getting-password2.png


Obtenir une réponse Oui/Non
------------------------------

Pour créer une fenêtre contextuelle invitant l'utilisateur à répondre par Oui ou par Non, utilisez la fonction ``get_yes_or_no``. Cette fonction retournera un booléen (``True`` s'ils ont cliqué sur Oui, ``False`` s'ils ont cliqué sur Non). Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``None``.

.. sourcecode:: python
    
    import easygui_qt as easy

    reponse = easy.get_yes_or_no("Combattez le monstre?")

.. image:: images/getting-yes-no1.png


**Options additionelles**

Si vous appelez ``get_yes_or_no`` avec un deuxième argument (séparé par une virgule), ce deuxième argument doit être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy

    reponse = easy.get_yes_or_no("Combattez le monstre?", "Combat")

.. image:: images/getting-yes-no2.png


Obtenir une valeur de couleur RVB/*RGB*
------------------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à sélectionner une couleur, utilisez la fonction ``get_color_rgb``. Cette fonction renverra une liste avec les valeurs RVB de la couleur sélectionnée. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie ``None``.

.. sourcecode:: python
    
    import easygui_qt as easy

    color = easy.get_color_rgb()

    r = color[0]    # accéder au montant dans le canal rouge
    g = color[1]    # accéder au montant dans le canal vert
    b = color[2]    # accéder au montant dans le canal bleu

.. image:: images/getting-color.png


Obtenir le chemin du nom de fichier/*Get File Nom Path*
-----------------------------------------------------------

Pour créer une fenêtre contextuelle qui invite l'utilisateur à sélectionner un fichier à partir de son ordinateur, utilisez la fonction ``get_file_name``. Cette fonction renverra une chaîne contenant le chemin complet du fichier sélectionné. Si l'utilisateur appuie sur *Annuler* ou ferme la fenêtre, cette fonction renvoie une chaîne vide ``''``.

.. sourcecode:: python
    
    import easygui_qt as easy

    selected_image = easy.get_file_name()

.. image:: images/getting-file-name1.png


**Options additionelles**

Si vous appelez ``get_file_name`` avec un deuxième argument (séparé par une virgule), ce deuxième argument doit être une chaîne et sera interprété comme le titre de la fenêtre contextuelle.

.. sourcecode:: python
    
    import easygui_qt as easy

    selected_image = easy.get_file_name("Choisi une Image")

.. image:: images/getting-file-name2.png


Afficher le texte formaté HTML
---------------------------------

Pour créer une fenêtre contextuelle affichant le rendu HTML, utilisez la fonction ``show_html``.

Cette fonction nécessite deux arguments, le titre de la fenêtre (sous forme de chaîne) et le code HTML à rendre (également une chaîne).

.. sourcecode:: python
    
    import easygui_qt as easy

    du_HTML = """
    <h1>Example</h1>
    <p>Ceci est juste un exemple de <em> certaines </em> des choses que vous pouvez faire lors du rendu HTML. Vous pouvez faire beaucoup plus de choses:</p>

    <ul>
        <li>autres balises/*tags* HTML que vous allez apprendre</li>
        <li>y compris les images</li>
        <li>beaucoup plus!</li>
    </ul>"""

    easy.show_html("Demo", du_HTML)

.. image:: images/showing-html.png


Display HTML Formatted Text
----------------------------

Pour créer une fenêtre contextuelle affichant le contenu d'un fichier au format HTML, utilisez la fonction ``show_file``.

Cette fonction nécessite trois arguments, le chemin du fichier (sous forme de chaîne), le titre de la fenêtre (sous forme de chaîne), le moteur de rendu à utiliser (également une chaîne).

.. sourcecode:: python

    import easygui_qt as easy

    file = "path/to/index.html"
    easy.show_file(file, "File Demo", "html")

.. image:: images/showing-file1.png


**Options additionelles**

Lorsque vous appelez la fonction ``show_file``, vous pouvez choisir entre les moteurs de rendu suivants:

- ``text``
- ``code``
- ``html``
- ``python``

.. sourcecode:: python
    
    import easygui_qt as easy

    file = "chemin/vers/du_script.py"
    easy.show_file(file, "File Demo", "python")


.. image:: images/showing-file2.png