# room_set_camera

With this function you can assign a camera to a specific viewport in a
room other than the current one. You supply the room index, the view
index (from 0 to 7) and then the index of the camera to use.

#### Syntax:

``` gml
room_set_camera(rm, vind, camera);
```

|          |                                                                                                                            |                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                                       | Description                                        |
| rm       |  [Room Asset](../../../../../The_Asset_Editors/Rooms)                                                                  | The index of the room to set the view camera of    |
| vind     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The index of the view port to assign the camera to |
| camera   |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The index of the camera to assign                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.myroom = room_add();
room_set_camera(global.myroom, 0, global.MainCam);
```

The above code assigns a camera in a newly created room to view port
\[0\].
