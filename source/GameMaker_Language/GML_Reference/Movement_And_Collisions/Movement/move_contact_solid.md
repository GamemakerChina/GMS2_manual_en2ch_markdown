# move_contact_solid

This function will move the instance running the code a set number of
pixels in the specified direction until it meets an instance with
[**solid**](../../Asset_Management/Instances/Instance_Variables/solid)
flagged as true. You can use -1 or 0 for the maxdist being a default
1000px, ie: GameMaker will move the instance continually up 1000 pixels
until it is out of collision.

#### Syntax:

``` gml
move_contact_solid( dir, maxdist );
```

|          |                                                                         |                                                                                      |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                          |
| dir      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The direction to move in.                                                            |
| maxdist  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum distance the object can travel (-1 or 0 a default value of 1000 pixels). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !place_meeting(x, y + 1, obj_Floor)
{
    move_contact_solid(270, -1);
}
```

The above code will check beneath the instance for a collision with
"obj_Floor", and if there is none, then it will move it down until there
is a collision, or 1000 pixels have been covered.
