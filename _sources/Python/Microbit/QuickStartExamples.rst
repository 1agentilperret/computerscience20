
.. qnum::
   :prefix: microbit-examples-
   :start: 1

.. _microbit_examples:

Micro:bit Reference
====================

There are no official docs yet, but here is a short quick-reference to get you started. These following demo code is from the `bito module readme file <https://github.com/whaleygeek/bitio>`_.

.. note:: There is a microbit.sleep(2000) at the end of some examples, because once your Python program finishes the bitio icon will be displayed on the micro:bit again and this will overwrite whatever is on the micro:bit screen.

Connecting to the micro:bit
----------------------------

.. sourcecode:: python
    
    # NOTE: Make sure bitio.hex is installed
    import microbit


Scrolling text on the screen
-----------------------------

.. sourcecode:: python
    
    import microbit
    microbit.display.scroll("Hello")
    microbit.sleep(2000)


Displaying a single character
---------------------------------

.. sourcecode:: python
    
    import microbit
    microbit.display.show("A")
    microbit.sleep(2000)


Displaying numbers
---------------------------------

.. sourcecode:: python
    
    import microbit
    microbit.display.scroll(2345)
    microbit.sleep(2000)


Displaying numbers using a 2-digit font
---------------------------------

.. sourcecode:: python
    
    import microbit
    for n in range(99):
        microbit.display.show(n)
        microbit.sleep(250)


Getting a list of pre-defined images
--------------------------------------

.. sourcecode:: python
    
    import microbit
    print(microbit.Image.STD_IMAGE_NAMES)
    microbit.sleep(2000)


Displaying a pre-defined image
--------------------------------------

.. sourcecode:: python
    
    import microbit
    microbit.display.show(microbit.Image.HAPPY)
    microbit.sleep(2000)


Spinning a clock
--------------------------------------

.. sourcecode:: python
    
    import microbit
    for c in microbit.Image.ALL_CLOCKS:
        microbit.display.show(c)
        microbit.sleep(250)

    
Defining a custom image
--------------------------------------

.. sourcecode:: python
    
    import microbit
    BANANA = microbit.Image("00090:00090:00990:09900:99000")
    microbit.display.show(BANANA)
    microbit.sleep(2000)


Clearing the display
--------------------------------------

.. sourcecode:: python
    
    import microbit
    microbit.display.clear()
    microbit.sleep(2000)


Sensing when a button is pressed
--------------------------------------

.. sourcecode:: python
    
    import microbit
    while True:
        if microbit.button_a.was_pressed():
            microbit.display.show("A")
            microbit.sleep(500)
            microbit.display.clear()

    
Sensing when a pin is touched
--------------------------------------

.. sourcecode:: python
    
    import microbit
    while True:
        if microbit.pin0.is_touched():
            microbit.display.show("T")
            microbit.sleep(500)
            microbit.display.clear()

    
Reading accelerometer values
--------------------------------------

.. sourcecode:: python
    
    import microbit
    while True:
        print(microbit.accelerometer.get_values())
        microbit.sleep(250)

  
Sensing tilt in the X plane
--------------------------------------

.. sourcecode:: python
    
    import microbit
    while True:
        x = microbit.accelerometer.get_x()
        x = abs(x)
        if x > 200:
            print("Tilted")
        else:
            print("Not Tilted")
        microbit.sleep(500)


Reading the temperature
--------------------------------------

.. sourcecode:: python
    
    import microbit
    while True:  
        print(microbit.temperature())
        microbit.sleep(500)