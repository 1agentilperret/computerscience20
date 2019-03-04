.. qnum::
   :prefix: input-output-assn
   :start: 1


Projet entrée/sortie -- *Input/Output Assignment*
====================================================

.. topic:: Aperçu rapide de la journée

    Révisez les problèmes de pratique de la dernière lecon. Travaillez sur un premier projet Python, axée sur les **entrées/sorties**, les types de données et les conditions.


.. reveal:: curriculum_addressed_input_output_assn
    :showtitle: Résultats du programme d'études traités dans cette section. 
    :hidetitle: Cacher les résultat du programme

    - **CS20-CP1** Apply various problem-solving strategies to solve programming problems throughout Computer Science 20.
    - **CS20-FP1** Utilize different data types, including integer, floating point, Boolean and string, to solve programming problems.
    - **CS20-FP2** Investigate how control structures affect program flow.


Que fait ce programme?
---------------------------

Rappelez-vous qu'un seul signe égal ``=`` est utilisé pour **assigner** une valeur. Deux signes égaux ``==`` sont utilisés pour **comparer** une valeur.


.. note:: Votre enseignant peut choisir d'utiliser les exemples suivants comme activité de classe, en les affichant et en vous demandant de deviner ce que chacun va faire avant d'exécuter le code.


Que vont produire les programmes suivants? Pourquoi?

.. activecode:: wdtpd_input_output_first_assn_1
    :caption: Que va imprimer ce programme?
    :nocodelens:

    print(16 == "16")


Pouvez-vous voir l'erreur dans l'exemple suivant? Comment pourriez-vous résoudre ce problème?

.. activecode:: wdtpd_input_output_first_assn_2
    :caption: trouvez l'erreur et corrigez-la!
    :nocodelens:

    nom = input("Quel est votre nom? ")
    if nom == sarah:
      print("Salut Sarah! Ravi de te voir!")


.. activecode:: wdtpd_input_output_first_assn_3
    :caption: Que va imprimer ce programme?
    :nocodelens:

    nombre = input("Quel nombre devrions-nous doubler? ")
    valeur_double = nombre * 2
    print(valeur_double)




Soyez prudent avec les types de données
------------------------------------------

Rappelez-vous que lorsque vous prenez les entrées de l'utilisateur avec la fonction ``input()``, la valeur est **toujours, toujours une chaîne!** Si vous devez effectuer une sorte de calcul mathématique avec l'entrée de l'utilisateur, vous devez convertir l'entrée en un nombre (*int* ou *float*). Rappelez-vous que les fonctions disponibles pour la conversion de type sont les suivantes:

- ``int(x)`` pour convertir *x* en entier
- ``float(x)`` pour convertir *x* en nombre à virgule flottante (nombre avec une décimale)
- ``str(x)`` pour convertir *x* en chaîne (une valeur entourée de guillemets)


Exemple de projet d'entrée/sortie
--------------------------------------

.. note:: Vous avez maintenant eu l'occasion de vous entraîner à un certain nombre de problèmes impliquant de saisir une entrée de l'utilisateur, d'effectuer une opération sur cette entrée et d'imprimer un résultat. Ce pourrait être un bon moment pour mettre en pratique les connaissances que vous avez acquises. Une tâche possible est donnée ci-dessous.

*Vous pouvez travailler directement dans le manuel ou utiliser Thonny. Quoi qu'il en soit, veillez enregistrer votre solution dans votre dossier Informatique 20 à la fin de la journée!*

Ecrivez un programme Python qui convertira les *degrés Celsius en degrés Fahrenheit* **ET** de *Fahrenheit en Celsius*.

Votre programme devrait demander à l'utilisateur quelle conversion vous souhaitez effectuer (de F à C ou de C à F), puis saisir une valeur en degrés Celsius/Fahrenheit et générer la valeur convertie en degrés Fahrenheit/Celsius.

Pour ce premier projet, vous n'avez pas besoin d'un programme qui saisie uniuquement les chiffres (en d'autres termes, vous pouvez supposer que l'utilisateur entrera juste un nombre). Cela signifie que si l'utilisateur va entrer ``bob`` lorsque vous lui demandez la température, votre programme se bloquerait, ce qui ne pose pas de problème pour ce programme.

Comme il s’agit de le premier projet Python que vous allez soumettre, les notes suivantes peuvent être utiles:

- veillez inclure un en-tête de commentaire dans votre code, ce qui signifie que votre fichier Python devrait commencer par quelque chose comme:


    # Projet de conversion de température
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici
 

** Extras pour les experts**

- essayez de vérifier l’entrée de l’utilisateur (en d’autres termes, assurez-vous que votre programme ne plante pas si l’utilisateur saisit "Frank" au lieu de 15 à la demande de température). *NOTE: consultez la structure **try and except control** en Python. Vous voudrez probablement rechercher sur Internet quelques idées à ce sujet.*
- ajouter également la possibilité de convertir à partir de Kelvin (donc choisir de quelle unité convertir ensuite choisir vers quelle unité convertir).


.. activecode:: first_input_output_assignment_scratch_work_area
    :nocodelens:
    :enabledownload:

    # Projet de conversion de température
    # Mettez votre nom ici
    # Mettez la date ici

    # votre code va ici


Évaluation
-----------


.. reveal:: eval_eighty_five_python_one
    :showtitle: Évaluation pour avoir 85%
    :hidetitle: Cacher l'évaluation pour avoir 85%

    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Critère                                                                                                                                       | oui  | non (-10%)  | un peu (-5%) |
    +===============================================================================================================================================+======+=============+==============+
    | Votre programme Python demande à l'utilisateur quelle conversion il/elle souhaiterait effectuer ((1) de F à C ou (2) de C à F)                |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Votre programme Python saisi une valeur de l'utilisateur en degrés Celsius/Fahrenheit                                                         |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Votre programme Python converti les degrés *Celsius en Fahrenheit*                                                                            |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Votre programme Python converti les degrés *Fahrenheit en Celsius*                                                                            |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Votre programme Python a suffisemment de commentaires pour expliquer à un autre programmeur ce que chaque partie de ton code fait             |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    | Votre programme Python a des espaces blaches dans le code pour faciliter la lecture par un autre programmeur                                  |      |             |              |
    +-----------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+--------------+
    
    


.. reveal:: eval_one_hundy_python_one
    :showtitle: Évaluation pour avoir 100%
    :hidetitle: Cacher l'évaluation pour avoir 100%
   
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Critère                                                                                                                                                             | oui  | non (-10%)  | un peu (-5%)|
    +=====================================================================================================================================================================+======+=============+=============+
    | Votre programme Python demande à l'utilisateur **de** quelle unité il/elle souhaiterait convertir ([1] Celcius [2] Fahrenheit [3] Kelvin)                           |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python demande à l'utilisateur **vers** quelle unité il/elle souhaiterait convertir ([1] Celcius [2] Fahrenheit [3] Kelvin)                         |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python saisi une valeur de l'utilisateur en degrés Celsius/Fahrenheit/Kelvin                                                                        |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python converti les degrés *Celsius en Fahrenheit et Kelvin*                                                                                        |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python converti les degrés *Fahrenheit en Celsius et Kelvin*                                                                                        |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python converti les degrés *Kelvin en Fahrenheit et Celsius*                                                                                        |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python a suffisemment de commentaires pour expliquer à un autre programmeur ce que chaque partie de ton code fait                                   |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
    | Votre programme Python a des espaces blaches dans le code pour faciliter la lecture par un autre programmeur                                                        |      |             |             |
    +---------------------------------------------------------------------------------------------------------------------------------------------------------------------+------+-------------+-------------+
