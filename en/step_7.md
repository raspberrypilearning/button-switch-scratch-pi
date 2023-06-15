## Challenge: which LED?

For this challenge, you will write a completely new code that randomly chooses one of three LEDs to turn on when you press the button.

--- no-print ---

![An animation of a button being pressed resulting in a red, green or yellow LED being lit randomly](images/whichLED_completedTask.gif)

--- /no-print ---

--- print-only ---

![A button being pressed resulting in one of three LEDs being lit randomly](images/whichLED_completedTask.png)

--- /print-only ---

You need to wire up three LEDs (preferably different colours) and a button.

To keep the code simple, connect the LEDs to three consecutive number GPIO pins, e.g. 4, 5, and 6.

![A breadboard with a button, three LEDs and three resistors. The button is connected to GPIO pin 2 and a ground pin. The LEDs all span the bridge of the breadboard. Their ground legs are all connected to Raspberry Pi ground pins. The three LED's positive legs are each connected to a resistor and the resistors are connected to GPIO pins 4, 5 and 6 respectively](images/whichLED_3LEDsAnd1button.png)

NOTE: In addition to using the drop-down box, you can also specify an LED number by dropping in a variable block, as shown below.

```blocks3
turn LED (my variable) [on v] :: extension
```

See if you can use this to make one random LED turn on when you press the button and then, after a moment, turn off again.

--- hints ---

--- hint ---

First, create a `variable`{:class="block3variables"} and call it `random_LED`{:class="block3variables"}.

Then write code so that `when you press button 2`{:class="block3extensions"}, `random_LED`{:class="block3variables"} is set to `between 4 and 6`{:class="block3operators"}, a `random_LED`{:class="block3variables"} turns on, the program `waits`{:class="block3control"} for `0.2 seconds`{:class="block3control"} and then the same `random_LED`{:class="block3variables"} turns off again.

--- /hint ---

--- hint ---

These are the code blocks you will need, but you will need to put them in the correct sequence.

```blocks3
pick random (4) to (6)
turn LED (0) [on v] :: extension
random_LED
random_LED
set [random_LED v] to (0)
turn LED (0) [off v] :: extension
when button (2 v) is [pressed v] ::hat extension
wait (0.2) seconds
```

--- /hint ---

--- hint ---

Write your program using the code below.

```blocks3
when button (2 v) is [pressed v] ::hat extension
set [random_LED v] to (pick random (4) to (6))
turn LED (random_LED) [on v] :: extension
wait (0.2) seconds
turn LED (random_LED) [off v] :: extension
```

--- /hint ---

--- /hints ---
