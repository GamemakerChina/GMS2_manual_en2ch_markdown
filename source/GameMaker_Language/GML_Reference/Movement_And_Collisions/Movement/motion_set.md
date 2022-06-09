# motion_set

This function sets a new direction of movement and a new speed to the
instance running the code. Note that this *does not* add to the
instances current speed and direction (for that you would use [
motion_add() ](motion_add) ) but rather forces it to the new
settings.

#### Syntax:

``` gml
motion_set(dir, speed);
```

|          |                                                                         |                    |
|----------|-------------------------------------------------------------------------|--------------------|
| Argument | Type                                                                    | Description        |
| dir      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new direction. |
| speed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new speed.\`   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if irandom(9) = 1
{
    motion_set(random(360), 1 + random(3));
}
```

This above code will make the instance change speed and direction at
random intervals.
