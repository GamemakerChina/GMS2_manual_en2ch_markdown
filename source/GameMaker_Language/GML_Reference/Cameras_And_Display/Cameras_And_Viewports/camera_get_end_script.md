# camera_get_end_script

This function can be used to retrieve the ID of the [script
function](../../../GML_Overview/Script_Functions) assigned as the
end function for the given camera. If no script function is assigned
then the function will return -1.

#### Syntax:

``` gml
camera_get_end_script(camera_id)
```

|           |                                                                                                                            |                                                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                     |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera |

#### Returns:

``` gml
 Script Function

or -1 if no function is assigned
```

#### Example:

``` gml
var scr = camera_get_end_script(camera_view[0]);
if scr != cutScene
{
    camera_set_update_script(camera_view[0], cutScene);
}
```

The above code checks the script function assigned as the begin script
for the camera assigned to view port\[0\] and if it is not "cutScene" it
is set to that function.
