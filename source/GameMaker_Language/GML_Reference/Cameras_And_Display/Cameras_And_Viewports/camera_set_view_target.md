# camera_set_view_target

You can use this function to set the follow target of the view camera
within the room. You give the unique camera ID value (as returned by the
different [ camera_create() ](camera_create) functions) and then
give the target instance or object ID that you wish to set the camera
view to. Note that if you choose an object ID and there is more than one
instance of that object in the room, there is no way for GameMaker to
know which instance you wish to follow and so it could be any of them.

#### Syntax:

``` gml
camera_set_view_target(camera_id, instance_id/object_id)
```

|                       |                                                                                                                                                                                         |                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument              | Type                                                                                                                                                                                    | Description                                                     |
| camera_id             |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)                                                               | The unique camera ID value returned when you created the camera |
| instance_id/object_id |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | Instance or object to have the camera target for following      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_view_target(view_camera[0], id);
```

The above code will set the view camera target for the camera assigned
to view port\[0\] to that of the instance running the code.
