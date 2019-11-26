## Controlling an LED sequence

In the last section, **controlling an LED**, you used a button to turn an LED on and off. Now you are going to use the button to control an LED running a flashing sequence.

You can keep the same hardware setup that you used in **controlling an LED**. If you like, you can easily adapt the project and add extra LEDs or a buzzer.

![Button and LED circuits](images/controlSequence_buttonAndLED.png)

### Flashing while pressed

For your first sequence control project, you'll code the LED to flash only while the button is pressed.

--- task ---

First, you'll need an event such as the `when flag clicked`{:class="block3events"} block.

Underneath that, place a `forever`{:class="block3control"} loop and inside that, place an `if... then`{:class="block3control"} block.

```blocks3
when flag clicked
forever
    if <> then
    end
end
```

--- /task ---

This set of blocks will continuously check a condition, or ask a question, and then do something if the condition is **true**, i.e. the answer is positive. In this case you want to ask if the button attached to GPIO pin 2 is being pressed.

--- task ---

Add a `Rapsberry Pi`{:class="block3extensions"} **selection** block, that asks if a `button is pressed`{:class="block3extensions"}. Set the button number to `2`{:class="block3extensions"}.

```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
    end
end
```

--- /task ---

Now you need to fill the gap after `then`{:class="block3control"} with what happens if the condition is **true**, i.e. if the button is being pressed.

In this example, the LED will flash, but it could be whatever you like.

--- task ---

Add blocks to `turn LED 4 on`{:class="block3extensions"}, `wait 0.1 seconds`{:class="block3control"} (a tenth of a second), `turn LED 4 off`{:class="block3extensions"} and then `wait`{:class="block3control"} again.

```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
+       turn LED (4 v) [on v] ::extension
+       wait (0.1) seconds
+       turn LED (4 v) [off v] ::extension
+       wait (0.1) seconds
    end
end
```

Click the green flag and press the button. Keep the button pressed and see what happens.

--- /task ---

The code only says to turn the LED on and off when the button is being pressed but as long as the button is pressed those instructions will keep repeating, making the LED flash.

Since the last LED instruction is to `turn LED 4 off`{:class="block3extensions"}. The LED will always be off when the button is not being pressed.

--- task ---

Reverse the position of the two `turn LED 4 on & off`{:class="block3extensions"} blocks.

Can you see what effect this will have?

```blocks3
when flag clicked
forever
    if <button (2 v) is [pressed v]?> then
+       turn LED (4 v) [off v] ::extension
        wait (0.1) seconds
+       turn LED (4 v) [on v] ::extension
        wait (0.1) seconds
    end
end
```

Click the green flag, press the button and se what has changed.

--- /task ---

### Flashing until pressed

For your second sequence control project, you'll code the LED to flash continuously until the button is pressed.

--- task ---

First, you'll need an event such as the `when flag clicked`{:class="block3events"} block.

Underneath that, place a `forever`{:class="block3control"} loop and inside that, place an `if... then`{:class="block3control"} block.

```blocks3
when flag clicked
forever
+   if <> then
    else
    end
end

<button (2 v) is [pressed v]?> :: extension

turn LED (4 v) [on v] ::extension
wait (0.1) seconds
turn LED (4 v) [off v] ::extension
wait (0.1) seconds
```

--- /task ---
