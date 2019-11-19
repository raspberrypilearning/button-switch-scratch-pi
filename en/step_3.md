## A random button

Looking at the example code from **Button basics**, there are three different effects happening all at the same time. 

+ size 
+ colour
+ whirl

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

--- task ---

From the `Operators`{:class="block3operators"} block palette, add a `pick random 1 to 10`{:class="block3operators"} block and change the range to 1 to 3.

```blocks3
when button (2 v) is [pressed v] ::extension
set [random_effect v] to (pick random (1) to (3))
```
Now, every time you press the button, `random_effect`{:class="block3variables"} is set to 1, 2 or 3.

--- /task ---

### About selection

At this point in the code, you need the program to make a **decision**. You need it to decide which of the three effects is going to happen each time the button is pressed. We call this decidion a **selection**.

The program asks a question, checks the answer and then proceeds one way or another depending on the answer. The answer to a selection question can only be **true** or **false**.

Question: Does `random_effect`{:class="block3variables"} equal `1`{:class="block3variables"}?

The answer is either **true** (yes, `random_effect`{:class="block3variables"} equals `1`{:class="block3variables"}) or **false** (no, `random_effect`{:class="block3variables"} does **not** equal `1`{:class="block3variables"}). There are no other options.

`If`{:class="block3control"} it is 1, then the program will do one thing, `else`{:class="block3control"} (otherwise) it will something else.

Let's add some selection to your program.

--- task ---

From the `Control`{:class="block3control"} block palette, add an `If... then... else`{:class="block3operators"} block.

```blocks3
when button (2 v) is [pressed v] ::extension
set [random_effect v] to (pick random (1) to (3))
If <> then
else
end
```

--- /task ---




