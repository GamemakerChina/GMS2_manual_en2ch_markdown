# window_set_colour

This function can set the background colour of the game window. This
colour represents that which will be used for those areas of the game
window that are not occupied by any views. The following image
illustrates this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/window_set_colour.png)  
The above image has two views with two view ports, each one drawn at
different positions. This stretches the game window to accommodate both
ports and uses the window colour to colour the background where no view
is shown.

#### Syntax:

``` gml
window_set_colour(colour);
```

|          |                                                                                                           |                               |
|----------|-----------------------------------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                                                      | Description                   |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to set the region. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if window_get_colour() != c_black
{
    window_set_colour(c_black);
}
```

The above code will check the window colour to see if it is set as black
or not, and if it is not it sets it to black.
