# skeleton_get_bounds

This function will return an array of values associated with any given
bounding box for the currently assigned skeleton animation sprite. You
supply the index number for the bounding box to get the details of (you
can retrieve the total number of bounding boxes for the sprite using the
function [ skeleton_get_num_bounds() ](skeleton_get_num_bounds) )
and the function will return an array with the following elements:

-   \[0\] - the number of points on the bounding box (a real)
-   \[1\] - the name of the bounding box (a string)
-   \[2\] - the x position of the first point
-   \[3\] - the y position of the first point
-   \[etc...\] - further x/y position data up to the number of points on
    the bounding box

NOTE The bounding box of a Spine sprite is set up in Spine itself, not
in GameMaker .

#### Syntax:

``` gml
skeleton_get_bounds(index);
```

|          |                                                                               |                                              |
|----------|-------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                          | Description                                  |
| index    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The bounding box index to get the values of. |

#### Returns:

``` gml
 Array

(minimum 2 elements: numPoints, name [, xPos, yPos, etc...])
```

#### Example:

``` gml
var num = skeleton_get_num_bounds();
var yy = 60;
for(var i = 0; i &amp;lt; num; i++)
{
    var b_info = skeleton_get_bounds(i);
    if b_info[0] &amp;gt; 0
    {
        var data = b_info[1] + ":";
        for(var j = 0; j &amp;lt; b_info[0]; j++)
        {
            data += " (" + string(b_info[(j * 2) + 2]) + ", " + string(b_info[(j * 2) + 2 + 1]) + ")";
        }
        draw_text(20, yy, data);
        yy += 20;
    }
}
```

The above code will loop through each of the bounding boxes associated
with the currently assigned sprite and then draw that data as a string
to the screen.
