## Challenge: A more random button

Add to, and edit, the code from **A random button** so that there is a fourth random option **and** also that the whirl effect changes a random amount so that it can whirl in either direction.

The fourth random option will be shrinking.

--- no-print ---

![Random effects](images/moreRandom_completedTask.gif)

--- /no-print ---

--- print-only ---

![Random effects](images/moreRandom_completedTask.png)

--- /print-only ---

Start with the [code](http://rpf.io/p/en/button-switch-scratch-pi-get){:target="_blank"} from [A random button](http://rpf.io/p/en/button-switch-scratch-pi-get){:target="_blank"}.

```blocks3
when button (2 v) is [pressed v] ::extension
set [random_effect v] to (pick random (1) to (3))
If <(random_effect)=(1)> then
    change size by (50) %
else
    If <(random_effect)=(2)> then
        change [color v] effect by (20)
    else
        change [whirl v] effect by (50)
    end
end
```

Look at how you have coded three options already. How will you add a fourth?

Adding to the whirl effect value makes the sprite whirl in an anti-clockwise direction. How can you also make the sprite whirl in the opposite, clockwise, direction?

--- hints ---

--- hint ---

For an extra random option, the `random_effect`{:class="block3variables"} will need to have `4`{:class="block3variables"} possibilities rather than `3`{:class="block3variables"}.

Previously you coded what would happen `if`{:class="block3control"} `random_effect`{:class="block3variables"} `= 1`{:class="block3operators"} and `if`{:class="block3control"} `random_effect`{:class="block3variables"} `= 2`{:class="block3operators"}. Now you need to add that `if`{:class="block3control"} `random_effect`{:class="block3variables"} `= 3`{:class="block3operators"}, `then`{:class="block3control"} `change size`{:class="block3looks"} by a `negative` number to make it shrink.

Remember that if `random_effect`{:class="block3variables"} is not 1, 2 or 3 then it must be 4.

To make the `whirl`{:class="block3looks"} go either way, `change`{:class="block3looks"} it by `a random number`{:class="block3operators"} from `-100`{:class="block3operators"} to `100`{:class="block3operators"}. A negative number takes away from the `whirl`{:class="block3looks"} effect value making it whirl in a clockwise direction.

--- /hint ---

--- hint ---

You will need to add or edit the blocks below. These are all blocks already in your code so you can save some time by duplicating parts of your existing code.

![Light show challenge code parsons problem](images/lightShow_lightShowCode__parsons.png)

You might also want to use the `random number`{:class="block3operators"} block.

![Light show challenge code parsons problem](images/lightShow_randomNumber.png)

--- /hint ---

--- hint ---

The code below are some possible examples but what you come up with is up to you. You might want to think about the result you want and try to make that heppen with code, or you could approach it from the other side, playing with the code and seeing what the results look like. 

Always try and understand why the result look the way it does. 

![Light show challenge code solution](images/lightShow_lightShowCode_Solution.png)

--- /hint ---

--- /hints ---
