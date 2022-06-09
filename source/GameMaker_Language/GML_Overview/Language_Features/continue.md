# continue

The continue statement has the following basic syntax:

``` gml
continue;
```

If used inside of a statement that forms a loop ( [ for ](for) , [
repeat ](repeat) , [ while ](while) or [ do / until
](do___until) ), it will immediately end the current iteration and
jump back to the beginning of the loop starting a new iteration and
omitting any code that comes after the continue within the loop. It can
also be used within the [ with ](with) statement, where it will
cause the code to skip to the next instance and run again. Note that if
continue is used outside of any of these contexts it will give an error.
Below is an example of use in a for loop:

``` gml
var _val = 0;

for (var i = 0; i &amp;lt; 10; i += 1)
{
    if (val_array[i] &amp;lt;= 0)
    {
        continue;
    }
    _val += val_array[i];
}

draw_text(32, 32, "Positive Values Total = " + string(_val));
```

Below is an example of use in a while loop:

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

Below is an example of use in a do / until loop:

``` gml
do
{
    var _x = random(room_width);
    var _y = random(room_height);

    if (instance_position(_x, y, obj_Enemy)
    {
        continue;
    }

    instance_create_layer(_x, _y, "Instances", obj_Enemy);
}
until (instance_count(obj_Enemy) &amp;gt;= 10);
```

Below you can find an example of use in a repeat loop:

``` gml
repeat(10)
{   
    var _x = random(room_width);
    var _y = random(room_height);

    if (instance_position(_x, y, obj_Enemy)
    {
        continue;
    }

    instance_create_layer(_x, _y, "Instances", obj_Enemy);
}
```

Finally, an example of use in a with statement:

``` gml
with (obj_Enemy_Parent)
{
    if (object_index == obj_Enemy_InDestructible)
    {
        continue;
    }

    hp -= 100;

    if (hp &amp;lt;= 0)
    {
        instance_destroy();
    }
}
```
