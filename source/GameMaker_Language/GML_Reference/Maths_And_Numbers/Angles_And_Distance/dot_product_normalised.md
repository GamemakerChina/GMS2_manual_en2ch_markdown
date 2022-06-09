# dot_product_normalised

The dot product is a value expressing the angular relationship between
two vectors and is found by taking two vectors, multiplying them
together and then adding the results. The name "dot product" is derived
from the centered dot "·" that is often used to designate this operation
(the alternative name "scalar product" emphasizes the scalar rather than
vector nature of the result). The actual mathematical formula can be
written like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/dot_product_image.png)  
So, in 2D the dot product of vectors a\[x1,y1\] and b\[x2,2\] is x1x2 +
y1y2 , meaning that the dot_product in GameMaker is calculated as:

``` gml
a · b = (x1*x2)+(y1*y2);
```

What about the *normalised* dot product? The normalised dot product has
been corrected in such a way as to bring the return value into the range
of -1 and 1 (see the section on
[Vectors](../../../../Additional_Information/Vectors) for more
detailed information), which is exceptionally useful in many
circumstances, particularly when dealing with lighting and other 3D
functions.

#### **Syntax:**

``` gml
dot_product_normalised(x1, y1, x2, y2)
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the first vector.  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the first vector.  |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the second vector. |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the second vector. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var x1, y1, x2, y2; x1 = lengthdir_x(1, image_angle); y1 = lengthdir_y(1, image_angle); x2 = o_Player.x - x; y2 = o_Player.y - y; if dot_product_normalised(x1, y1, x2, y2) &amp;gt; 0 seen=true else seen=false;
```

The above code creates a vector using the instances image angle, and
then gets the vector of the player object "o_Player" to itself. Finally
it calculates the dot product of these two vectors and if it is greater
than 0 it sets the variable "seen" to true, and if it is equal to or
less than 0 it sets it to "false".
