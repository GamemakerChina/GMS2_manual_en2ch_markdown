# Number Functions

Real numbers in GameMaker are considered *double-precision
floating-point numbers* - that is to say that they have a decimal point
in them with no fixed number of digits either before or after the
point - or *integers* - that is to say they are whole numbers with no
decimal point value. 2, for example, is an integer but 2.01 is a
floating point real. **NOTE** : On the **HTML5** target, all real
numbers are doubles. This distinction between integers and floats is
very important when dealing with cross platform development as the
precision of calculations made on a Windows PC is *not* the same as the
precision of those same calculations when made on a mobile device. This
means that you should pay particular attention when making comparisons,
for example:

``` gml
if (image_index == 1)
{
    do something...
}
```

In the example above, if we have been setting the image_speed to 0.25 -
for example - then after four steps you may assume that the image_index
value would be 1, but it *may* be a value like 1.0000002 due to the way
floating point maths works and so the evaluation will not be true .
These types of errors can be quite hard to debug and so it is always
good to be aware of them and to plan ahead and use other means of
checking values or to use the appropriate flooring or rounding functions
(listed below) to convert the number to check into an integer (for more
information on floating point maths and why this is an issue, please
[see here](https://floating-point-gui.de/) ). For example the above code
could be written as:

``` gml
if (floor(image_index) == 1)
{
    do something...
}
```

It is also worth noting that when using the **YoYo Compiler** targets,
all expressions and functions are *evaluated from left to right* , while
on all other target platforms they are evaluated *from right to left* ,
meaning that this - for example - will give different results depending
on the platform:

``` gml
val = max(num, ++num, num++);
```

**NOTE** : For more informaton, see the section on [Evaluation
Order](../../../GML_Overview/Evaluation_Order) . You can also use a
special function available in GameMaker to set the **epsilon** value for
floating point maths. When a real number is rounded to the nearest
floating point number, the epsilon (also know as "machine epsilon")
forms an upper bound on the relative error, and you can get and set the
epsilon value using the following functions:

-   [math_set_epsilon](math_set_epsilon)
-   [math_get_epsilon](math_get_epsilon)

These functions all deal with using random numbers and values: ** NOTE
** When using the random functions, GameMaker maintains the same random
seed every time you start the game. This makes debugging much easier as
you are guaranteed that the random functions will always initially
return the same value, however should you not wish this to happen, you
must first set a new random seed at the very start of the game, either
using [ randomise() ](randomise) or [ random_set_seed()
](random_set_seed) .

-   [choose](choose)
-   [random](random)
-   [random_range](random_range)
-   [irandom](irandom)
-   [irandom_range](irandom_range)
-   [random_set_seed](random_set_seed)
-   [random_get_seed](random_get_seed)
-   [randomise](randomise)

These are all functions that will round values in some way, or select a
single value from various given values:

-   [round](round)
-   [floor](floor)
-   [frac](frac)
-   [abs](abs)
-   [sign](sign)
-   [ceil](ceil)
-   [max](max)
-   [mean](mean)
-   [median](median)
-   [min](min)
-   [lerp](lerp)
-   [clamp](clamp)

Finally we a miscellaneous collection of important mathematical
functions:

-   [exp](exp)
-   [ln](ln)
-   [power](power)
-   [sqr](sqr)
-   [sqrt](sqrt)
-   [log2](log2)
-   [log10](log10)
-   [logn](logn)
