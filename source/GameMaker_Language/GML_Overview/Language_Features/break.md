# break

The break statement is used to end prematurely a [ for ](for) , [
repeat ](repeat) , [ while ](while) or [ do / until
](do___until) loop of some kind, or to tell a [ switch ](switch)
statement to end at that point, or to prematurely end a [ with
](with) call. Please see the individual pages for these different
functions to get a more in-depth explanation of how it can be used under
each circumstance. Note that if break is used outside of any of these
contexts it will give an error. Below you can see a few basic examples
of how break can be used, and its syntax is simply:

``` gml
break;
```

break in a for loop:

``` gml
for (var i = 0; i &amp;lt; 10; i += 1)
{
    if (array[i] == 234)
    {
        break;
    }
}

num = i;
```

break in a repeat loop:

``` gml
var i = 0;
var temp = 0;
repeat (10)
{
    temp += array[i];
    if (temp &amp;gt; max_total)
    {
        break;
    }
    else
    {
        i += 1;
    }
}
```

break in a while loop:

``` gml
var i = 0;
while (!place_free(x, y))
{
    x = random(room_width);
    y = random(room_height);
    if (i &amp;gt; 50)
    {
        break;
    }
    else
    {
        i+=1;
    }
}
```

break in a do / until loop:

``` gml
var _id = noone;
do
{
    _id = list[| 0];
    if instance_exists(_id)
    {
        break;
    }
    ds_list_delete(list, 0);
}
until (ds_list_empty(list));
target = _id;
```

break when using with :

``` gml
var count = 0;
with (obj_Enemy)
{
    count++;
    if (count &amp;gt; 10)
    {
        break;
    }
    hp = 100;
}
```

break in a switch :

``` gml
switch (keyboard_key)
{
    case vk_left:
    case ord("A"):
        x -= 4;
    break;

    case vk_right:
    case ord("D"):
        x += 4;
    break;

    case vk_up:
    case ord("W"):
        y -= 4;
    break;

    case vk_down:
    case ord("S"):
        y += 4;
    break;
}
```
