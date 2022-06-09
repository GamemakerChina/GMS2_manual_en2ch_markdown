# skeleton_get_num_bounds

This function will return the number of bounding boxes associated with
the skeleton animation sprite assigned to the instance running the code.
This can then be used along with the function [ skeleton_get_bounds()
](skeleton_get_bounds) to retrieve data about each of the bounding
boxes. NOTE The bounding box of a Spine sprite is set up in Spine
itself, not in GameMaker .

#### Syntax:

``` gml
skeleton_get_num_bounds();
```

#### Returns:

``` gml
 Real
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
