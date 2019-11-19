## A random button

Looking at the example code from **Button basics**, there are three different effects happening all at the same time. 

```blocks3
when button (2 v) is [pressed v] ::extension
change size by (50) %
change [color v] effect by (10)
change [whirl v] effect by (50)

when [space v] key pressed
set size to (100) %
set [color v] effect to (0)
set [whirl v] effect to (0)
```

Now you're going to use **selection** and a variable to make only one of these things happen each time you press the button.

The `when space pressed`{:class="block3events"} code will remain unchanged as this is the reset code.

--- task ---

Make a new variable and name it `random_effect`{:class="block3variables"}.

--- no-print ---
![Make a new variable](images/randomButton_newVariable.gif)
--- /no-print ---

--- print-only ---
![Make a new variable](images/randomButton_newVariable.png)
--- /print-only ---

--- /task ---

--- task ---

Disconnect the `change`{:class="block3looks"} blocks from the `when button pressed`{:class="block3extensions"} event block and move them to one side.

```blocks3
when button (2 v) is [pressed v] ::extension

change size by (50) %
change [color v] effect by (10)
change [whirl v] effect by (50)
```

--- /task ---

--- task ---

Under your `when button pressed`{:class="block3extensions"} event, add a `set my variable to 0`{:class="block3variables"} block.

Change the variable to `random_effect`{:class="block3variables"} using the dropdown box.

--- no-print ---
![Change the variable](images/randomButton_changeVariable.gif)
--- /no-print ---

--- print-only ---
![Change the variable](images/randomButton_changeVariable.png)
--- /print-only ---

--- /task ---


