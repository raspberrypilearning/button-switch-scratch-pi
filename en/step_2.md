## Button basics

Button switches are an **input**. The Button sends a signal which is received by the Raspberry Pi to be processed.

![Input Output](images/buttonBasics_inputOutput.png)

In the previous **LEDs, buzzers and Scratch games** project we looked at using The Raspberry Pi's powerful genral purpose input output (GPIO) pins to use to control simple electronic **outputs** such as LEDs and buzzers. Now we are going to do the same for **inputs** with the humble button switch.

![Button switches](images/buttonBasics_buttonSwitches.png)

Many switches we use, such as most household light switches, **toggle** between `on` and `off`. All of the button switches in the image above, and the ones we'll be looking at in this project are **push-to-make** switches, meaning that they are `on` while they being pressed and `off` whenever they are not being pressed.

### Button switch leg connections

All but the smallest buttons have four legs which are connected in positive and negative pairs (polarity does not matter for button switches).

![Button switch in breadboard](images/buttonBasics_buttonInBB.png)

![Button switch leg connections](images/buttonBasics_buttonLegConnections.png)

Before you get using a switchable I/O (input/output) pin, you're going to light an LED by making a simple circuit using a 3.3v pin to supply the power.

This will make sure you know:
+ That your LED and resistor work
+ What a simple LED circuit looks like
+ How to connect the components together

A very simple LED circuit would be an LED connected to a battery cell with a resistor to protect the LED by limiting the current flow.

![LED circuit with battery and resistor](images/lightLED_batteryLedCircuit.png)

NOTE: The positive always connects to the longer, positive leg of the LED which is called the **anode**.

You will be using a breadboard to help connect the electronic components together. The image below shows the same circuit using a breadboard.

![LED circuit with battery, breadboard and resistor](images/lightLED_batteryBreadLedCircuit.png)

The breadboard holes are conncted in lines underneath the cover so that:
+ the blue wire connects to the resistor
+ the resistor connects to the **anode** (long, positive leg) of the LED
+ the **cathode** (shorter, negative leg) of the LED connects to the black wire

You are going to make this same circuit but using the Raspberry Pi as the power source instead of a battery.

--- task ---

Place an LED in your breadboard so that the legs are either side of the middle 'trench'. the breadboard is not connected across this gap.

Note which is the longer, positive leg. In the example the longer-legged anode is on the left.

![LED in breadboard](images/lightLED_ledInBb.png)

--- /task ---