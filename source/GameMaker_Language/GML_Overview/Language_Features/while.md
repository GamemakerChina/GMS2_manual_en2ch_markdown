# while

The GameMaker Language has a number of ways that you can perform *loops*
, one of the most important is the while loop. This loop function has
the form:

``` gml
while (&amp;lt;expression&amp;gt;)
{
    &amp;lt;statement&amp;gt;;
    &amp;lt;statement&amp;gt;;
    ...
}
```

Here you have a statement that is iterated over again and again based on
the results of the evaluation of an expression , ie: with a while loop,
as long as the expression evaluates to true , the statement (which can
also be a code block of multiple statements with curly brackets {} ) is
executed. Below you can find an example of a typical way to use "while":

``` gml
while (place_meeting(x, y, obj_Wall))
{
    x -= 1;
}
```

The above code is checking for a collision between the calling instance
and a "wall" instance, and it will perform multiple iteration s while
one is occurring - moving the instance left by one pixel - until the
instance is no longer in collision. **When should you use a while
loop?** It should be used any time you want to repeat one or more
statements, but don't actually know - or care - how many times it has to
repeat, keeping in mind that if the initial evaluation is false , the
statements may not even be run. Please not that you should **be very
careful with your while loops** ! You can easily make *infinite* loops,
in which case your game will hang and not react to any user input
anymore and need to be force closed. For example:

``` gml
while (!place_free(x, y))
{
    x = random(room_width);
    y = random(room_height);
}
```

Now, the above code may work fine, but it may also cause an infinite
loop if the instance is unable to find an empty position to move to, and
this will cause the game to hang. If you find yourself in a position
where this kind of thing is a possibility, then you should either use a
different non-blocking loop kind, or use an additional variable check in
the expression (you can use multiple expressions along with the [ and (&
& )](../Expressions_And_Operators) , [ or ( \|\|
)](../Expressions_And_Operators) and [ xor ( ^^
)](../Expressions_And_Operators) operator s for the check):

``` gml
var _check = 0;
while ((!place_free(x, y)) &amp;amp;&amp;amp; (_check &amp;lt; 100))
{
    x = random(room_width);
    y = random(room_height);
    _check += 1;
}
if _check &amp;gt;= 100
{
    // code failed, so deal with it
}
```

Alternatively you can use the [break](break) statement to break out
of the loop, for example, the following code will generate 100 random
numbers then continue, even though the while evaluation is *always*
going to be true :

``` gml
var i = 0;
while (true)
{
    x[i] = random(room_width);
    y[i] = random(room_height);
    if ((i++) &amp;gt;= 100)
    {
        break;
    }
}
```

You may also use the [continue](continue) statement in a while loop.
Using this will end the current loop iteration and restart the
loop again on a new iteration, for example:

``` gml
var file = file_text_open_read("Game_Data.txt");
var _num = 0;
while (!file_text_eof(file))
{
    var _s = file_text_readln(file);

    if (_s == "")
    {
        continue;
    }

    str[num++] = _s;
}

file_text_close(file);
```

This code above will open a file and read a line from it each loop
iteration until the end of the file contents are reached. If the line
being read is an empty string, the current loop iteration is ended using
the continue statement and a new iteration will be started, otherwise
the string is added into an [array](../Arrays) and the array
position incremented. For more examples of loop functions please see the
sections on [ repeat ](repeat) , [ do... until ](do___until) ,
and [ for ](for) .
