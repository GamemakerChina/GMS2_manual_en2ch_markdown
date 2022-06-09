# colour_get_hue

This function will return the hue of the given colour. This is the
"pure" colour tone which is part of the hue, saturation and value
(luminosity) method for defining a colour. The following image
illustrates how this value corresponds to the HSV scale of colour:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/get_hue.png)  

#### Syntax:

``` gml
colour_get_hue(col);
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
col = merge_colour(colour_get_hue(c_teal), c_white, 0.5);
```

The above code gets the hue used to make the colour constant "c_teal"
and then merges it with white at a 50:50 ratio, storing the resulting
colour in the variable "col".
