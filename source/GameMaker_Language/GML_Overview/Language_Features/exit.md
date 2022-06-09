# exit

The exit statement has the following syntax:

``` gml
exit;
```

exit simply ends the execution of the current
[script function](../Script_Functions) ,
[method](../Method_Variables) , or
[event](../../../The_Asset_Editors/Object_Properties/Object_Events)
. Note there is a slight difference in use here depending on the scope:

-   If you use exit in a script function or method it will simply exit
    the function and return to the code that called the function.
-   If you use exit in a code block within an object's event, it will
    exit *the entire event* even if there are various separate code
    blocks after exit has been called.
-   If you use exit in a parent event and call that event using [
    event_inherited()
    ](../../GML_Reference/Asset_Management/Objects/Object_Events/event_inherited)
    in a child object, only the parent event will exit and the child's
    event (which called event_inherited() ) will continue.

When used in an event, exit is typically used to avoid an instance
running any further code when a specific condition has been met (or
not). The code below outlines an example of how it could be used, in
this case within a Collision Event, although it can be used in any
event.

``` gml
if (!visible)
{
    exit;
}

other.hp -= attack;
other.coins -= 4;
coins += 4;
```

The above code checks if the current instance is not visible, in that
case it exits the code block, otherwise it goes ahead and runs the rest
of the code. **NOTE** : It does not end the execution of the game. For
that you need to use the function [ game_end()
](../../GML_Reference/General_Game_Control/game_end) .
