.. qnum::
   :prefix: string-quotes
   :start: 1


Quelles citations/*quotes* utiliser lors de la création de chaînes/*strings*
==============================================================================

.. topic:: Aperçu rapide de la journée

    Les chaînes à triple guillemet peuvent s'étendre sur plusieurs lignes et contenir d'autres types de guillemets. Travaillez sur un projet Python, axée sur les entrées/sorties de chaînes et des conditions.


.. reveal:: curriculum_addressed_string_quotes
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.


.. index:: string quotes

Un peu plus de détails sur les chaînes
------------------------------------------

Les chaînes en Python peuvent être placées entre guillemets simples (``'``) ou doubles quotes (``"`` - le caractère de guillemet double), ou trois des mêmes caractères de guillemets séparés (``'''`` ou ``"""``).

.. activecode:: ch02_4
    :nocanvas:

    print(type('Ceci est une chaîne.') )
    print(type("Celui-ci aussi.") )
    print(type("""et lui.""") )
    print(type('''et même celui là...''') )


Les chaînes entre guillemets peuvent contenir des guillemets simples à l'intérieur, comme dans  ``"La barbe à Bruce"``, et les chaînes simples peuvent avoir des guillemets doubles à l'intérieur, comme dans ``'Les chevaliers qui disent "Ni!"'``. Les chaînes entourées de trois occurrences de l'un ou l'autre des guillemets sont appelées des chaînes à triple citations/*triple quoted strings*. Ils peuvent contenir des guillemets simples ou doubles:

.. activecode:: ch02_5
    :nocanvas:

    print('''"Oh non", s'écria-t-elle, "le vélo de Ben est cassé!"''')

Les chaînes à triple citations peuvent même s'étendre sur plusieurs lignes:

.. activecode:: ch02_6
    :nocanvas:

    print("""Ce message s'étendra
    plusieurs lignes
    du texte.""")

Python s'en fiche si vous utilisez des guillemets simples ou doubles ou les trois guillemets pour entourer vos chaînes. Une fois qu'il a analysé le texte de votre programme ou votre commande, la façon dont il stocke la valeur est identique dans tous les cas, et les guillemets qui entour ne font pas partie de la valeur.

.. activecode:: ch02_7
    :nocanvas:

    print('Ceci est une chaîne.')
    print("""Et c'est la même chose.""")


Que fait ce programme?
---------------------------

.. note:: Votre enseignant peut choisir d'utiliser les exemples suivants comme activité de classe, en les affichant et en vous demandant de deviner ce que chacun fait avant d'exécuter le code.

Que vont produire les programmes suivants? Pourquoi?

Pouvez-vous corriger l'erreur dans les programmes suivants?

.. activecode:: wdtpd_other_input_methods_1
    :caption: Trouvez et corrigez l'erreur dans ce programme!
    :nocodelens:

    citation_de_chanson = 'Les Trois Accords, dans leur chanson "Saskatchewan", chantent "Saskatchewan; Tu m'as pris ma femme."'

    print(citation_de_chanson)


.. activecode:: wdtpd_other_input_methods_2
    :caption: Trouvez et corrigez les erreurs dans ce programme!
    :nocodelens:

    partie_un = "Les Trois Accords, dans leur chanson "Saskatchewan", chantent"
    partie_deux = 'Saskatchewan; Tu m'as pris ma femme.'

    print(partie_un + partie_deux)


.. activecode:: wdtpd_other_input_methods_3
    :caption: Trouvez et corrigez les erreurs dans ce programme!
    :nocodelens:

    citations_intéressantes = 'Il y a beaucoup de gens qui ont dit des choses intéressantes. Quelques citations amusantes incluent:
    
    "Ce que je ne peux pas créer, je ne comprends pas." - Richard Feynman
    "Juger un homme par ses questions plutôt que par ses réponses." - Voltaire
    "L'histoire est le total des choses qui auraient pu être évitées" - Konrad Adenauer

    print(citations_intéressantes)


.. note:: 

    Une autre alternative à la concaténation de chaînes consiste à utiliser des chaînes-f/*f-strings* (littéraux de chaîne formatés/*formatted string literals*). Une chaîne de caractères vous permet de facilement créer une chaîne contenant la *valeur* des variables insérées. Pour créer une chaîne de caractères, vous devez simplement mettre la lettre ``f`` avant les guillemets qui commencent la chaîne. Cela indique à Python qu'il doit rechercher les noms de variables à l'intérieur de la chaîne et s'il en trouve, il les remplacera par la valeur de cette variable. Pour que Python trouve la variable, vous devez la placer entre accolades, comme ``{une_variable}``. Considérons cet exemple d'utilisation d'une chaîne-f::

        nom = "Eli"
        age = 14

        salutation = f"Bonjour, {nom}. J'ai entendu dire que tu venais d'avoir {age}!"
        print(salutation)

        # ce code imprimera ce qui suit:
        # Bonjour, Eli. J'ai entendu dire que tu venais d'avoir 14 ans!


Temps de travail
---------------------

Veuillez passer le reste de la classe à continuer à travailler sur votre projet Python actuelle (probablement quelque chose mettant l’accent sur les entrées/sorties de l’utilisateur).
