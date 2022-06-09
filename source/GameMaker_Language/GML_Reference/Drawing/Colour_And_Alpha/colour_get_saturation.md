# colour_get_saturation

This function will return the saturation of the given colour. This is
the amount of the colour tone that is mixed into the final colour and is
part of the hue, saturation and value (luminosity) method for defining a
colour. The following image illustrates how this value corresponds to
the HSV scale of colour:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/get_sat.png)  

#### Syntax:

``` gml
colour_get_saturation(col);
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
col = make_colour_hsv(random(255), colour_get_sat(c_teal), 255);
```

The above code gets the saturation used to make the colour constant
"c_teal" and then uses that value to set a random colour to have the
same saturation, storing the resulting colour in the variable "col".
