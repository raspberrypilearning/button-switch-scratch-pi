## Controlling an LED

As we looked at earlier, button switches are an **input** that sends information to your Pi about the moment it is pressed or released and whether it is currently held down or not held down.

So far, the only **output** that you have used is effects on a Scratch sprite shown visually on a screen.

![Input Output](images/buttonBasics_inputOutput.png)

In the **LEDs, buzzers and Scratch games** project you looked at controlling **outputs** such as LEDs. Now you are going to combine your button **input** with an LED **output**.

--- no-print ---
![Button and LED](images/controlLED_completedTask.gif)
--- /no-print ---

--- print-only ---
![Button and LED](images/controlLED_completedTask.png)
--- /print-only ---

### The electronic circuits

Let's start with the simple button setup you already have.

![Simple button setup](images/controlLED_buttonToGPIO2.png)

--- task ---

Add an LED connected to GPIO pin 4.

![Added LED circuit](images/controlLED_LEDToGPIO4.png)

--- /task ---

**NOTE:** The two circuits, one for the button and one for the LED, are completely separate, independent circuits.

### The Scratch program

Now that you have our cicuits ready, it is time for you to write some code in Scratch.

--- task ---

From the `Rapsberry Pi Simple Electronics`{:class="block3extensions"} block palette, grab a `when button pressed`{:class="block3extensions"} block and set the button number to `2`{:class="block3extensions"}.

Add another block to `turn LED on`{:class="block3extensions"} and set the LED number to `4`{:class="block3extensions"}.

```blocks3
when button (2 v) is [pressed v] ::hat extension
turn LED (4 v) [on v] ::extension
```

--- /task ---
