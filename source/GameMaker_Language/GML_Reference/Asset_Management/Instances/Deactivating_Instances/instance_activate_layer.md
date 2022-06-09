# instance_activate_layer

With this function you can activate a layer that has been deactivated
previously. You need to supply the **layer ID** , which can either be
the name of the layer as written in the code editor (as a string) or the
actual layer ID value as returned by the [ layer_create()
](../../Rooms/General_Layer_Functions/layer_create) and all
deactivated instances on that layer will activated once again. Note that
if you have deactivated a layer that has persistent instances, you will
need to reactivate the layer again with this function before changing
room, otherwise any persistent instances will *not* be carried over and
will be discarded. Note too that activation is not instantaneous, and an
instance that has been activated in this way will not be considered to
be active until the end of the event in which the function was called.

#### Syntax:

``` gml
instance_activate_layer(layer_id);
```

|          |                                                                                                                                                                                                                  |                                                |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                    |
| layer_id |  [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id) or [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The layer name string (or ID value) to be used |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
instance_activate_all();
var _vx = camera_get_view_x(view_camera[0]);
var _vy = camera_get_view_y(view_camera[0]);
instance_deactivate_region(view_xview[0] - 64, view_yview - 64, _vx + 128, _vy + 128, false, false);
instance_activate_layer("Player_Layer");
```

The above code activates all instances within the room and then
deactivates those that are outside of the limits of the current camera
view, except for the instances on the layer "Player_Layer" which are
re-activated again at the end.
