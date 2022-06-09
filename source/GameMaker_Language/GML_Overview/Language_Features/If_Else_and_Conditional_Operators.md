# if / else and Conditional Operators

A fundamental feature of most programming languages is the ability to
ask a simple question that gives a boolean true or false answer, and in
GML this is achieved using the if keyword. A simple if condition takes
an expression and will perform one or more statement s if the expression
resolves as true , with the following basic form:

``` gml
if (&amp;lt;expression&amp;gt;)
{
    &amp;lt;statement&amp;gt;;
    &amp;lt;statement&amp;gt;;
    ...
}
```

Here you are saying that if an expression resolves as true then do
something. Note that the "then" part of the condition is *implicit* ,
but there is a then keyword that can be used (although it's almost
always omitted), so you can also create conditionals like this:

``` gml
if (&amp;lt;expression&amp;gt;) then
{
    &amp;lt;statement&amp;gt;;
    &amp;lt;statement&amp;gt;;
    ...
}
```

Apart from if and then , you can also use the else keyword to do
something else if the expression being checked evaluates as false . This
" if... then... else... " form looks like this:

``` gml
if (&amp;lt;expression&amp;gt;)
{
    &amp;lt;statement&amp;gt;;
}
else
{
    &amp;lt;statement&amp;gt;;
}
```

In this case the expression will be evaluated, and if it evaluates as
false , the statement after else is executed, otherwise the initial
statement is executed (it's true ). NOTE In the GameMaker language
any value that is less than or equal to 0 will evaluate as false , while
any value that is greater than 0 will evaluate as true . It is a good
habit to always put brackets around the expressions and curly brackets
{} around the statements in the if (otherwise only the first statement
will be executed), and take a new line in the block for each statement,
for example:

``` gml
// This will work
if &amp;lt;expression&amp;gt; &amp;lt;statement&amp;gt;;

// Example:
if test == true variable = false else variable = true;
```

``` gml
// This is better
if (&amp;lt;expression&amp;gt;)
{
    &amp;lt;statement&amp;gt;
}
else
{
    &amp;lt;statement&amp;gt;
}

// Example
if (test == true)
{
    variable = false;
}
else
{
    variable = true;
}
```

Note that while this is slightly more verbose, it means that there is no
ambiguity in the code and that it will compile correctly on ail
platforms at all times. However, the initial example may not, as
explained on the section in the [Expressions And
Operators](../Expressions_And_Operators) page. **NOTE** : When
comparing two values to see if they are equal, you should use the " == "
operator, and only use the " = " one for assignment. Currently GameMaker
will treat them as interchangeable, but this may change in the future
and your code is cleaner and more obvious when using the correct
operators for comparisons and assignments. To give a proper example of
using if , consider the following code which will move an instance
towards the position x=200 in the room when placed in the Step Event:

``` gml
if (x &amp;lt; 200)
{
    x += 4;
}
else
{
    x = 200;
}
```

Note that you can also do *compound* checks in an if , ie: check various
values or expressions in the same statement. These checks can use the
various [Combining Operators](../Expressions_And_Operators) ( &&
and, \|\| or, and ^^ xor). When you do this, GameMaker will evaluate
each of them one at a time, and depending on how they evaluate, then the
rest may be skipped. For example:

``` gml
if (keyboard_check_pressed(vk_enter)) &amp;amp;&amp;amp; (instance_exists(obj_Player))
{
    go = false;
    alarm[0] = room_speed;
}
```

Here we are checking using the && "and" operator, so it's checking if
*both* of the conditions in the if evaluate to true , and if the first
one is false then the second one won't even be checked. This is called
"short circuiting" the code, so when combining expressions to check, you
should ensure that the "cheapest" one for performance is always the
first to avoid evaluating the more expensive ones if the first evaluates
to false . In a similar vein, if a condition will can be evaluated as
true or false at compile time, then the entire condition will be removed
from the code, for example, say you have a
[macro](../Variables/Constants) DEBUG_ON for debugging and it can be
either true or false  - when it is set to false then the following code
block will be stripped from the game when it is compiled:

``` gml
if DEBUG_ON == true
{
    show_debug_message("Instances = " + string(instance_count));
}
```

You can also perform **conditional operations** (also know as
**ternary** operations), which are essentially a "shortcut" way of
performing a basic if . It has the following syntax:

``` gml
variable = &amp;lt;condition&amp;gt; ? &amp;lt;statement1 (if

 true

)&amp;gt; : &amp;lt;statement2 (if

 false

)&amp;gt;
```

The conditional operator " ? " will return one of two given values
depending on whether the condition expression evaluates to true or false
, for example:

``` gml
var temp_x = (x &amp;lt; (room_width / 2)) ? 32 : (room_width - 32);
```

The above code will check the value of "x" against the value of half the
room width and then if it is less it will set " temp_x " to 32 otherwise
" temp_x " will be room width - 32. Here are a few more examples of use:

``` gml
draw_text(x, y, "The fee is " + (global.Member ? "$2.00" : "$10.00"));
path_start(((global.level &amp;gt; 10) ? path_hard : path_easy;), 2, path_action_reverse, true);
(--hp &amp;lt;= 0) ? instance_destroy() : score += 10;
```

It is worth noting too that you can nest conditional operations but that
if you do then each operation will need to be enclosed in brackets, for
example:

``` gml
var c = a ? "foo" : (b ? "bar" : "whee"); // Correct
var c = a ? "foo" : b ? "bar" : "whee";   // Will cause an error
```
