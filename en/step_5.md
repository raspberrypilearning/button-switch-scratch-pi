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

And to turn the LED off again.

--- task ---

Duplicate the code you just wrote, change the `when button pressed`{:class="block3extensions"} to `when button released`{:class="block3extensions"}, and change the `turn LED 4 on`{:class="block3extensions"} to `turn LED 4 off`{:class="block3extensions"}.


```blocks3
when button (2 v) is [pressed v] ::hat extension
turn LED (4 v) [on v] ::extension

+ when button (2 v) is [released v] ::hat extension
+ turn LED (4 v) [off v] ::extension
```

--- /task ---

NOTE: The `when button pressed`{:class="block3extensions"} and `when button pressed`{:class="block3extensions"} blocks are constantly checking if the button is pressed or released. In the background they are acting like `forever`{:class="block3control"} loops, constantly checking the state of the button.

You can write your own code to do much the same thing. Next, you're going to write code that constantly 'asks' if the button is being pressed and tells the LED to be on or off depending on the answer.

--- task ---

Throw your previous code away.

Grab a starting event, the `when flag clicked`{:class="block3events"} block.

Underneath that, place a `forever`{:class="block3control"} loop and inside that, place an `if... then... else...`{:class="block3control"} block.

```blocks3
when flag clicked
forever
    if <> then
    else
    end
end
```

--- /task ---

Between the `if`{:class="block3control"} and the `then`{:class="block3control"} goes the condition to be checked.

--- task ---

From the `Rapsberry Pi Simple Electronics`{:class="block3extensions"} block palette, take a hexagonal `button is pressed`{:class="block3extensions"} block, place this in the haxagonal space and set the button number to `2`{:class="block3extensions"}.


```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
    else
    end
end
```
```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
    else
    end
    if + <button (2 v) is [pressed v]?> then
    else
    end
    if <+ button (2 v) is [pressed v]?> then
    else
+   if <button (2 v) is [pressed v]?> then
    else
    end
    end
end
```
--- /task ---

After the `then`{:class="block3control"} and after the `else`{:class="block3control"} go the responses to whether `button 2 is pressed`{:class="block3extensions"} or not.

--- task ---

In the first space, after `then`{:class="block3control"}, place a `turn LED 4 on`{:class="block3extensions"} block, and in the second space, after `else`{:class="block3control"}, place a `turn LED 4 off`{:class="block3extensions"} block.

```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
+          turn LED (4 v) [on v] ::extension 
    else
+          turn LED (4 v) [off v] ::extension    
    end
end
```

--- /task ---