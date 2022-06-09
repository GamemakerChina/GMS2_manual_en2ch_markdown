# instance_furthest

This function will check all the instances of the given object to see
which is furthest from the given x/y point. All checks will be from the
given x/y position to the *origin* (the x/y position) of instances of
the object specified. If no instances of the object exist, the function
will return the keyword
[noone](../../../GML_Overview/Instance_Keywords) , but if there are
instances then it will return the [ id ](Instance_Variables/id) of
the instance found. Please note that if the instance running the code
has the same object index as the object being checked, then it will be
included in the check (this includes checks for parent objects if the
calling instance is also a child of the parent).

#### Syntax:

``` gml
instance_furthest(x, y, obj);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position to check for instances far from. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position to check for instances far from. |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)           | The object to check for instances of.           |

#### Returns:

``` gml
 Instance ID

or

 noone
```

#### Example:

``` gml
var inst;
inst = instance_furthest(x, y, object_index);
if inst != id
{
    draw_line(x, y, inst.x, inst.y);
}
```

The above code will find the furthest instance that shares the same
object index as the instance running the code and store the id in a
variable. This variable is then checked to see if it is the same as the
id of the calling instance and, if it is not, a line is drawn between
the two instances.
