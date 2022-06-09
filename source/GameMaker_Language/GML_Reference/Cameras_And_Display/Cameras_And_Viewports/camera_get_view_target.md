# camera_get_view_target

This function can be used to retrieve the follow target of the given
camera. The return value can be an object index, an instance ID or -1 if
no follow target has been set.

#### Syntax:

``` gml
camera_get_view_target(camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
 Object Asset

,

 Instance ID

or -1
```

#### Example:

``` gml
var target = camera_get_view_target(view_camera[0]);
if target != obj_Player
{
    camera_set_view_target(view_camera[0], obj_Player);
}
```

The above code retrieves the follow target of the camera assigned to
view port\[0\] and then checks this to see if it matches the object
index "obj_Player". If it does not then the view camera is set to follow
an instance of that object.
