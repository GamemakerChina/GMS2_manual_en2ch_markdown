# merge_colour

With this function you can take two colours and then merge them together
to make a new colour. The amount of each of the component colours can be
defined by changing the "amount" argument, where a value of 0 will
return the first colour (col1), a value of 1 will return the second
colour (col2) and a value in between will return the corresponding mix.
For example, a value of 0.5 will mix the two colours equally. The
following image illustrates how this works by merging the colours red
and blue together:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/merge_colour.png)  

#### Syntax:

``` gml
merge_colour(col1, col2, amount);
```

|          |                                                                                                           |                                                                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                                                                                         |
| col1     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The first colour to merge                                                                                                                           |
| col2     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The second colour to merge                                                                                                                          |
| amount   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | How much of each colour should be merged. For example, 0 will return col1, 1 will return col2, and 0.5 would return a merge of both colours equally |

#### Returns:

``` gml
 Colour
```

#### Example:

``` gml
col = merge_colour(c_lime, c_orange, 0.5);
```

The above code uses the function to create a colour by merging lime and
orange 50/50 and then stores its value in the variable "col" for later
use.
