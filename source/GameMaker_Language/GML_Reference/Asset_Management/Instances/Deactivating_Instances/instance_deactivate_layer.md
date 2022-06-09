# instance_deactivate_layer

With this function you can deactivate all instances assigned to a
specific layer. You need to supply the **layer ID** , which can either
be the name of the layer as written in the code editor (as a string) or
the actual layer ID value as returned by the [ layer_create()
](../../Rooms/General_Layer_Functions/layer_create) , and note that
you can only deactivate *instance* layers with this function. Note that
if you have deactivated a layer that has instances of objects flagged as
**Persistent** , then you will need to reactivate the layer again with
the function [ instance_activate_layer() ](instance_activate_layer)
before changing room, otherwise any persistent instances on the layer
will *not* be carried over and will be discarded. Note too that
deactivation is not instantaneous, and an instance that has been
deactivated in this way will not be considered to be inactive until the
end of the event in which the function was called. **NOTE** : If you
deactivate an instance on room start (ie:from the room creation code, or
from an instance create event of an instance within the room) all
instances that are placed within the room from the room editor **will
still run their create event** before being deactivated. **WARNING** :
Deactivating instances that have physics enabled will **NOT** stop their
fixtures from interacting within the physics simulation. For that you
should set their [ phy_active
](../../../Physics/Physics_Variables/phy_active) variable to true or
false as you activate/deactivate the instances.

#### Syntax:

``` gml
instance_deactivate_layer(obj);
```

|          |                                                                                                                                                                                                                  |                                                |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                    |
| layer    |  [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id) or [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The layer name string (or ID value) to be used |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
instance_deactivate_layer("Enemy Layer");
var _vx = camera_get_view_x(view_camera[0]);
var _vy = camera_get_view_y(view_camera[0]);
var _vw = camera_get_view_width(view_camera[0]);
var _vh = camera_get_view_height(view_camera[0]);
instance_activate_region(_vx - 64, _vy - 64, _vw + 128, _vh + 128, false);
```

The above code deactivates all instances assigned to the layer
"Enemy_Layer" and then activates a region within the room.
