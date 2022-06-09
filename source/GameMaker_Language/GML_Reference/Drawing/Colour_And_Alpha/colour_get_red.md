# colour_get_red

This function returns the amount of red used to make the given colour,
with the value being between 0 and 255, where 0 is no red and 255 is all
red. The following image illustrates this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/get_red.png)  

#### Syntax:

``` gml
colour_get_red(col);
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
r_comp = colour_get_red(c_teal);
```

The above code will get the red component of the colour constant
"c_teal" and store the value in the variable "r_comp".
