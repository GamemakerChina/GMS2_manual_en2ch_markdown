# colour_get_value

This function will return the value (luminosity) of the given colour.
This is the amount of the "light" that is mixed into the final colour
and is part of the hue, saturation and value method for defining a
colour. The following image illustrates how this value corresponds to
the HSV scale of colour:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/get_val.png)  

#### Syntax:

``` gml
colour_get_value(col);
```

|          |                                                                                                           |                     |
|----------|-----------------------------------------------------------------------------------------------------------|---------------------|
| Argument | Type                                                                                                      | Description         |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to check |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
col = make_colour_hsv(random(255), 255, colour_get_value(c_teal));
```

The above code gets the value used to make the colour constant "c_teal"
and then uses that value to set a random colour to have the same
luminosity, storing the resulting colour in the variable "col".
