# camera_set_proj_mat

This function will set the **projection matrix** for a given camera. You
give the unique camera ID value (as returned by the different [
camera_create() ](camera_create) functions) and a projection matrix
to be applied. You can find out more about creating projection matrices
from the section [Matrix
Functions](../../Maths_And_Numbers/Matrix_Functions/Matrix_Functions)
, specifically
[matrix_build_projection_perspective()](../../Maths_And_Numbers/Matrix_Functions/matrix_build_projection_perspective)
and [ matrix_build_projection_ortho()
](../../Maths_And_Numbers/Matrix_Functions/matrix_build_projection_ortho)
. There are some things you need to keep in mind when using this
function:

-   If your camera does automatic object tracking - ie: it has been
    created using [ camera_create_view() ](camera_create_view) with
    an object index / instance ID that isn't -1, or you are setting a
    camera defined in the Room Editor, or you are setting the default
    camera - then this matrix will get overwritten the next game frame.
-   If you use this function to switch to a perspective projection (as
    opposed to the default orthographic projection), automatic drawing
    of tiled sprites will stop working and will need to be handled
    manually. This includes any background layers that use horizontal or
    vertical tiling and the
    [draw_sprite_tiled()](../../Drawing/Sprites_And_Tiles/draw_sprite_tiled)
    and
    [draw_sprite_tiled_ext()](../../Drawing/Sprites_And_Tiles/draw_sprite_tiled_ext)
    functions, which will only draw the sprite once instead of tiling it
    if a perspective projection is being used.

#### Syntax:

``` gml
camera_set_proj_mat(camera_id, matrix)
```

|           |                                                                                                                            |                                                                  |
|-----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument  | Type                                                                                                                       | Description                                                      |
| camera_id |  [Camera ID](../../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/Cameras_And_Viewports/camera_create)  | The unique camera ID value returned when you created the camera. |
| matrix    |  [Matrix Array](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Matrix_Functions/Matrix_Functions)   | The unique matrix ID returned when you created the matrix.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
view_camera[0] = camera_create();
var viewmat = matrix_build_lookat(640, 240, -10, 640, 240, 0, 0, 1, 0);
var projmat = matrix_build_projection_ortho(640, 480, 1.0, 32000.0);
camera_set_view_mat(view_camera[0], viewmat);
camera_set_proj_mat(view_camera[0], projmat);
```

The above code creates a new camera and assigns it to view port\[0\].
This camera then has its view and projection matrices set.
