.. qnum::
   :prefix: scratch-intro
   :start: 1


Introduction à Scratch (envoyer à tous)
============================================

.. topic:: Aperçu rapide de la journée

    Introduction au cours, et à l'environnement Scratch. Explique le plan de coordonnées utilisé dans Scratch et les blocs de mouvement de base. Présentez l'idée d'utiliser le bloc de diffusion pour envoyer des messages, qui est utilisé pour contrôler le déroulement du programme.


.. reveal:: curriculum_addressed
    :showtitle: Résultats du programme d'études traités dans cette section. 

    - **20IN-PT.1** Appliquer diverses stratégies de résolution de problèmes pour résoudre des problèmes de programmation dans le cours Informatique 20.
    - **20IN-FP.2** Faire des recherches sur la manière dont les structures de contrôle affectent le déroulement du programme.


Introduction
----------------------------

Bienvenue! Le but de ce cours est de vous apprendre à résoudre des problèmes, et nous utiliserons les concepts de l'informatique pour atteindre cet objectif. À la fin de la session, vous serez en mesure de résoudre les problèmes en toute confiance en écrivant des programmes informatiques. En d'autres termes, vous serez en mesure de contrôler ce que l'ordinateur fait en écrivant des algorithmes (une série d'étapes).

Bien que nous finirons par écrire du texte brut dans un fichier pour créer des programmes informatiques, ce processus peut être un peu intimidant. Pour vous aider à comprendre ce que vous êtes capable d'enseigner à un ordinateur, nous suivrons le processus suivant:

- utiliser un environnement de programmation visuel (cela vous permettra de comprendre les structures de contrôle de base de l'informatique et vous évitera de faire des erreurs de syntaxe qui amèneraient votre programme à signaler une erreur lorsque vous l'exécutez)
- utilisez un langage contraint pour résoudre les puzzles algorithmiques (ici vous tapez du texte pour contrôler ce que fait l'ordinateur, ce qui signifie que vous rencontrerez des erreurs de syntaxe, mais les énigmes que vous résolvez vous donneront un retour visuel instantané)
- utiliser un langage informatique "traditionnel" (une fois que vous vous sentirez confiant avec de nombreuses idées de base de l'informatique, nous les appliquerons en utilisant un langage informatique traditionnel)

Votre premier programme informatique!
--------------------------------------

Il existe de nombreux environnements de programmation visuelle différents, mais celui que nous utiliserons s'appelle `Scratch <https://scratch.mit.edu/>`_. Votre première tâche consiste à créer un compte sur le site Web Scratch, afin que les programmes que vous écrivez puissent être sauvegardés et consultés plus tard. 
`Allez faire cela maintenant! <https://scratch.mit.edu/>`_  

Si vous préférez regarder une vidéo, la `vidéo <https://www.youtube.com/watch?v=pJYCRtSDJSk>`_ suivante montre les mêmes idées que celles que j'ai décrites dans le texte ci-dessous.

.. youtube:: pJYCRtSDJSk
    :height: 315
    :width: 560
    :align: left
    :http: https

Maintenant que vous avez un compte, faisons votre premier programme informatique du semestre! Cliquez sur le bouton Créer en haut du site Web Scratch pour **créer** un nouveau projet.

.. image:: images/scratch_create.png

Dans la vue du projet, l'écran est divisé en plusieurs volets, y compris la scène (où vous verrez votre projet s'exécuter), la liste des lutins (montre quels lutins font partie de votre projet, et vous permet de les sélectionner), palette de blocs (voici tous les blocs que vous pouvez glisser et déposer sur vos scripts), et la zone des scripts (où vous allez combiner des blocs de code pour créer des programmes pour vos lutins à exécuter). L'une des choses les plus importantes à garder à l'esprit est que **vous ne pouvez pas briser l'environnement**, alors n'hésitez pas à explorer autant que vous voulez!

.. image:: images/scratch_areas.png

.. sidebar:: Note de l'enseignant

    You may want to spend some time exploring the environment with the students before you actually create the first program.

For our first program, let's create a simple conversation between two sprites. To do this, you'll need to add a second sprite to the project. You do this in a number of ways, each of which have an icon at the top of the sprite list pane. You can hover over each of the images with your mouse to discover what they represent. For now, use the "Choose Sprite from Library" icon to add an additional sprite to the stage.

.. image:: images/scratch_add_new_sprite_from_library.png

For this example, I included the Giga sprite, so my stage looks like this:

.. image:: images/scratch_initial_characters.png

.. note:: Once you have more than one sprite in the sprite list pane, you will be able to see that the scripts area pane shows the script for the currently selected sprite. To be sure you understand this, drag a block from the block palette onto the scripts area. Now select a different sprite in the sprite list by clicking on it. Notice how the blocks in the scripts area change when you select a different sprite.

Now that you have two sprites in the sprite list pane, let's get them to have a simple conversation. Select the **Looks** tab in the block palette, then drag a **say "Hello" for 2 secs** block to the scripts area. A quick way to see the result of this block is by double clicking it. Try it now! *Note that the small image of the cat is intended to show which sprite is selected in the Sprite List when dragging the block from the Block Palette to the Scripts Area.*

.. image:: images/scratch_say_block.png

Of course, we don't want to have to double click the block to make the conversation happen, so we need to have an event trigger the say block. Select the **Events** tab in the block palette, then drag a **when flag clicked** block into the scripts area. Now, drag the **say "Hello" for 2 secs** block until it snaps onto the **when flag clicked** block. At this point, you should be able to make your sprite say Hello when you click the flag above the stage.

.. image:: images/scratch_blocks_connected.png

Before we move on with the conversation, we should know how to delete things. If you have a block in your Scripts Area that you no longer want, simply drag it back to the Block Palette and release the mouse.

.. image:: images/scratch_deleting_a_block.gif

To get our conversation going, drag one sprite to the left side of the stage, and the other to the right side of the stage. Now, let's set their starting locations. Hook up the character on the left side of the stage to a block, as follows:

.. image:: images/scratch_goTo_1.png

The character on the right side of the stage should have the a script similar to this:

.. image:: images/scratch_goTo_2.png

.. note::
  Notice that Scratch uses the Cartesian plane (the xy grid system you learned in math class), and that the origin is directly in the centre of the stage, as shown below:

  .. image:: images/scratch_coordinate_plane.png
     :align: center

Drag both sprites to the locations you would like them to be when they are going to have the conversation. Notice that the x and y values in the *Go to* block in the block palette updates with the x and y locations of the sprite when you release the mouse. Now hook a **glide 1 secs to x: y:** block to the bottom of the script of the character coming in from the left hand side of the stage. Then drag a **say Hello! for 2 secs** block from the Looks tab onto the bottom of that, to have the character start the conversation. Finally, drag a **broadcast** block from the Events tab and hook it onto the bottom of the script. It should now look something like this:

.. image:: images/scratch_goTo_andGlide.png

Broadcasts
----------

What is the point of that broadcast block that we added to the script? In this situation, we wanted the second sprite (the one entering from the right side of the screen) to do something **once an action performed by another sprite was completed**. Broadcasts let us send messages, and any sprite (including the sprite that sent the message) within our project can listen for that message, and respond accordingly. This time, what we'd like to have happen is for the second sprite to enter the screen after the first sprite has moved to the middle of the screen and said something.

.. note:: Broadcasts are a simple way to introduce the idea of the event-driven programming paradigm. Although much of this course will be using the procedural programming paradigm, it is really helpful to be understand the basic concept of responding to user events!

To have another sprite listen for a broadcast, click on the sprite that you would like to react to the broadcast, then drag a *when I receive* block from the **Events** tab of the block palette to the scripts area. We could have the character do anything we want, but for this example, let's make our characters have a simple conversation. Recreate the following, and click the Green flag.

.. image:: images/scratch_when_i_receive.png

We can hook up as many chained broadcasts as we like. For example, in the example shown below, both characters react to the flag being clicked by going to their starting locations. After that, the chain of events is controlled by the following broadcasts:

- Giga Enters
- Cat Replies
- Goodbye

.. image:: images/scratch_conversation_complete.png

Notice as well that any number of sprites can react to the same broadcast. In the above example, only one sprite reacts to the Giga Enters and Cat Replies broadcasts. For the Goodbye broadcast, however, both the Cat and Giga react by hiding.

Check Your Understanding
~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: scratch_broadcast_check_1
   :answer_a: The current sprite would say "Go"
   :answer_b: The current sprite would say "Go", then say "Green!"
   :answer_c: The current sprite would say "Green!", then say "Go"
   :answer_d: The current sprite would say "Green!"
   :correct: b
   :feedback_a: Although this would happen, it is not the only thing! Consider what happens when the broadcast is sent.
   :feedback_b: Yes! The sprite would say "Go" for 1 second, then broadcast <em>first</em>, which it would respond to by saying "Green!" for 1 second.
   :feedback_c: No, it will say "Go" first (since that is the first thing in the chunk of code that executes when the flag is clicked).
   :feedback_d: It will do this, but it will say "Go" first (since that is the first thing in the chunk of code that executes when the flag is clicked).

   What would happen when you click the green flag, given the code below?

   .. image:: images/scratch_broadcast_check_1.png


.. mchoice:: scratch_broadcast_check_2
   :answer_a: The current sprite would say "Go" for 1 second, say "Green!" for 1 second, then move 10 steps.
   :answer_b: The current sprite would say "Go" for 1 second, move 10 steps, then say "Green!" for 1 second after the sprite stops moving.
   :answer_c: The current sprite would say "Go" for 1 second, then simultaneously move 10 steps and say "Green!" for 1 second.
   :correct: c
   :feedback_a: No, sending the broadcast will will cause the second chunk of blocks to execute, but will not stop the first chunk of code from continuing to execute. In other words, Scratch will not wait for the broadcast to be resolved before completing the rest of the chunk of code (in this case, the move 10 steps block).
   :feedback_b: No, both the say "Green" block and the move 10 steps block will happen simultaneously.
   :feedback_c: Yes, sending the broadcast will will cause the second chunk of blocks to execute, but will not stop the first chunk of code from continuing to execute.

   What would happen when you click the green flag, given the code below?

   .. image:: images/scratch_broadcast_check_2.png



.. mchoice:: scratch_broadcast_check_3
   :answer_a: The current sprite would say "Go" for 1 second, say "Green!" for 1 second, then move 10 steps.
   :answer_b: The current sprite would say "Go" for 1 second, move 10 steps, then say "Green!" for 1 second after the sprite stops moving.
   :answer_c: The current sprite would say "Go" for 1 second, then simultaneously move 10 steps and say "Green!" for 1 second.
   :correct: a
   :feedback_a: Yes! Since we are now using a broadcast and wait block, Scratch will pause the execution of the chunk of code that sent the broadcast until all scripts that reacted to the broadcast being sent have finished executing. 
   :feedback_b: No, the broadcast happens before the move, so the sprite will say "Green" before it moves.
   :feedback_c: No, since we are using a broadcast and wait block, the two scripts will not run simultaneously this time.

   What would happen when you click the green flag, given the code below?

   .. image:: images/scratch_broadcast_check_3.png



Practice Problem
-----------------

Make a new Scratch project. Save it as ``Conversation``. Pick at least two sprites, and make them have a little conversation. Be sure to use **broadcasts** to control the flow of your program!

If you want a bit more of a challenge, explore the blocks palette and incorporate some other blocks that haven't been discussed yet!
