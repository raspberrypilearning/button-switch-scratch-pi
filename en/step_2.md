## Button basics

Button switches are an **input**. The Button sends a signal which is received by the Raspberry Pi to be processed.

![Input Output](images/buttonBasics_inputOutput.png)

In the previous **LEDs, buzzers and Scratch games** project we looked at using The Raspberry Pi's powerful genral purpose input output (GPIO) pins to use to control simple electronic **outputs** such as LEDs and buzzers. Now we are going to do the same for **inputs** with the humble button switch.

![Button switches](images/buttonBasics_buttonSwitches.png)

Many switches we use, such as most household light switches, **toggle** between `on` and `off`. All of the button switches in the image above, and the ones we'll be looking at in this project are **push-to-make** switches, meaning that they are `on` while they being pressed and `off` whenever they are not being pressed.

### Button switch leg connections

All but the smallest buttons have four legs which are connected in signal in and signal out pairs (polarity does not matter for button switches).

![Button switch in breadboard](images/buttonBasics_buttonInBB.png)

In the image above, a **signal in** jumper cable could be connected anywhere in row 23 and the **signal out** cable anywhere in row 25.

NOTE: if you connected a cable to the left-side row 23 and another to the right-side of row 23, the signal would pass straight through the switch whether it was pressed or not.

![Button switch leg connections](images/buttonBasics_buttonLegConnections.png)

### A simple button set up

--- task ---

Plug a button switch into your breadboard. The button switches fit very well with legs spread across the middle trench in the breadboard.

![Button on breadboard diagram](images/buttonBasics_buttonInBBdiagram.png)

--- /task ---

--- task ---

Connect one leg (signal in) to a numbered GPIO pin. It is connected to GPIO pin 2 in the example

![connect to GPIO pin 2](images/buttonBasics_buttonToGpio2.png)

--- /task ---

--- task ---

Connect the other leg on that side (signal out) to a ground (GND or -) pin.

![connect to a ground pin](images/buttonBasics_buttonToGround.png)

--- /task ---

### Scratch controlled by the button

