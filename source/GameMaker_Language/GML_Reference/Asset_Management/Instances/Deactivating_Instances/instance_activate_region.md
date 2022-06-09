# instance_activate_region

With this function you can define a region within the room to activate
instances that have previously been deactivated. This region can either
be flagged as "inside" or "outside" as demonstrated in the following
image:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Instances/instance_activate_region.png)  
You can see in the image above that the "apple" instance is always
active because, even if the sprite itself doesn't overlap the region,
the bounding box does. So, instances are considered to be within the
region specified when their *bounding box* overlaps with it, and the
state of the collision mask (precise or not) is not taken into
consideration. Note that activation is not instantaneous, and an
instance that has been activated in this way will not be considered to
be active until the end of the event in which the function was called.

#### Syntax:

``` gml
instance_activate_region(left, top, width, height, inside);
```

|          |                                                                               |                                                                                          |
|----------|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Argument | Type                                                                          | Description                                                                              |
| left     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of the left of the rectangular region to activate.                      |
| top      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of the top of the rectangular region to activate.                       |
| width    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The width of the region to activate.                                                     |
| height   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The height of the region to activate.                                                    |
| inside   |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to activate instances on the inside of the region (true) or the outside (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
instance_deactivate_all(true);
var _vx = camera_get_view_x(view_camera[0]);
var _vy = camera_get_view_y(view_camera[0]);
var _vw = camera_get_view_width(view_camera[0]);
var _vh = camera_get_view_height(view_camera[0]);
instance_activate_region(_vx - 64, _vy - 64, _vw + 128, _vh + 128, false);
```

The above code deactivates all instances except the one that is running
the code and then activates a region within the room.
