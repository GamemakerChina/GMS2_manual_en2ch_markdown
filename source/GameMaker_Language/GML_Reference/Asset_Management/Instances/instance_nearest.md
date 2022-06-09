# instance_nearest

This function will check all the instances of the given object to see
which is nearest to the given x/y point. All checks will be from the
given x/y position to the *origin* (the x/y position) of instances of
the object specified. If no instances of the object exist, the function
will return the keyword [ noone
](../../../GML_Overview/Instance_Keywords) , but if there are
instances then it will return the [ id ](Instance_Variables/id) of
the instance found. Please note that if the instance running the code
has the same object index as the object being checked, then it will be
included in the check (this includes checks for parent objects if the
calling instance is also a child of the parent).

#### Syntax:

``` gml
instance_nearest(x, y, obj);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position to check from.         |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position to check from.         |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)           | The object to check for instances of. |

#### Returns:

``` gml
 Instance ID

or

 noone
```

#### Example:

``` gml
var inst, xx;
xx = x;
x -= 10000;
inst = instance_nearest(xx, y, object_index);
if inst != id
{
    draw_line(x, y, inst.x, inst.y);
}
x += 10000;
```

The above code move the current instance 10000 pixels then check its
previous position to find the nearest instance of the same object type.
If that instance is itself, it will do nothing more than move back to
its original position, but should the instance found be different, it
will draw a line between the two.
