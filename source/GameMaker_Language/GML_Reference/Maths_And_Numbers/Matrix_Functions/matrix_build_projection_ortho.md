# matrix_build_projection_ortho

This function builds an orthographic projection matrix based on the
specified parameters listed below (this is the default projection method
used when you create a room in GameMaker without changing anything).
Sometimes you need to switch from a perspective projection to an
orthographic projection which is what this function is for. It is
typically used to draw an overlay, for example, to show the score or
other aspects as this gives a "flat" view of the elements drawn (ie: no
perspective) in a 3D game. See the image below to get an idea of the
difference between orthographic and perspective views. **NOTE** : You
may also need to temporarily switch off hidden surface removal if you
want the information to be drawn regardless of the current depth
value.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/ortho_persp_image.png)  

#### Syntax:

``` gml
matrix_build_projection_ortho(width, height, znear, zfar);
```

|          |                                                                         |                               |
|----------|-------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                    | Description                   |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The width of the projection.  |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The height of the projection. |
| znear    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The near clipping plane.      |
| zfar     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The far clipping plane.       |

#### Returns:

``` gml
 Matrix Array
```

#### Example:

``` gml
viewmat = matrix_build_lookat(640, 240, -10, 640, 240, 0, 0, 1, 0);
projmat = matrix_build_projection_ortho(640, 480, 1.0, 32000.0);
camera_set_view_mat(view_camera[0], viewmat);
camera_set_proj_mat(view_camera[0], projmat);
```

The above code creates a new look-at matrix and orthographic matrix,
stores their IDs in local variables and then uses them to set the view
and projection matrices for the camera assigned to view port\[0\].
