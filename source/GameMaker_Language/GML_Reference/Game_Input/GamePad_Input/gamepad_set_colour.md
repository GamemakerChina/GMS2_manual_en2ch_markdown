# gamepad_set_colour

This function can be used to set the colour of the LEDs within a
PlayStation controller. You specify the device slot to set, and then
give a colour, which can be any of the [colour
constants](../../Drawing/Colour_And_Alpha/Colour_And_Alpha) or a
colour value created using the specific colour functions or a HEX
value(like $FFFFFFF).

#### Syntax:

``` gml
gamepad_set_colour(device, colour);
```

|          |                                                                                                           |                                     |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                      | Description                         |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | Which gamepad device "slot" to set. |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to use.                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if health &amp;lt; 10
{
    gamepad_set_colour(0, c_red);
}
```

The above code will set the PlayStation controller LEDs to red if the
health variable falls below 10.
