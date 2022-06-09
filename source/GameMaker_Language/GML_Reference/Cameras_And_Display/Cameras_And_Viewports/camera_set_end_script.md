# camera_set_end_script

This function can be used to set a [script
function](../../../GML_Overview/Script_Functions) that will be
called at the end of every game frame that the camera is assigned to a
visible and active view port, after everything for that view camera has
been rendered. You give the unique camera ID value (as returned by the
different [ camera_create() ](camera_create) functions) and the ID
of the function to be called. The order in which functions attached to
cameras and the actual rendering of the camera view is as follows:

-   The cameras for all visible and active view ports have their
    **update function** called
-   Then for each view:
    -   The **begin function** for the camera for that view is called
    -   The draw events are executed for that view
    -   The **end function** for the camera is called
-   Move to the next active visible view and repeat...

#### Syntax:

``` gml
camera_set_end_script(camera_id, script)
```

|           |                                                                                                                            |                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera. |
| script    |  [Script Function](../../../../../GameMaker_Language/GML_Overview/Script_Functions)                                    | The script to run each game frame                                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
camera_set_end_script(view_camera[0], endCamera);
```

The above code sets the end script for the camera assigned to view port
\[0\].
