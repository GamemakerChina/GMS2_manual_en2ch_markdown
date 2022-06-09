# colour_get_green

This function returns the amount of green used to make the given colour,
with the value being between 0 and 255, where 0 is no green and 255 is
all green. The following image illustrates this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/get_green.png)  

#### Syntax:

``` gml
colour_get_green(col);
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
g_comp = colour_get_green(c_teal);
```

The above code will get the green component of the colour constant
"c_teal" and store the value in the variable "g_comp".
