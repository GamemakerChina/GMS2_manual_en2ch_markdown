# Background Layers

The GameMaker [Room Editor](../../../../../The_Asset_Editors/Rooms)
permits you to add backgrounds into any given room using *layers* . As
the name implies, a background layer is simply a sprite asset that is
being used as a background on a layer at a set depth within the room,
and by stacking layers you can make some things draw over or under
others. You can also control certain aspects of layers from code, adding
or removing things, or changing certain properties of the layer or what
it contains at run time. Below is a list of all the functions that can
be used for editing [**background
layers**](../../../../../The_Asset_Editors/Room_Properties/Layer_Properties)
:

-   [layer_background_get_id](layer_background_get_id)
-   [layer_background_exists](layer_background_exists)
-   [layer_background_create](layer_background_create)
-   [layer_background_destroy](layer_background_destroy)
-   [layer_background_visible](layer_background_visible)
-   [layer_background_sprite](layer_background_sprite)
-   [layer_background_htiled](layer_background_htiled)
-   [layer_background_vtiled](layer_background_vtiled)
-   [layer_background_stretch](layer_background_stretch)
-   [layer_background_blend](layer_background_blend)
-   [layer_background_alpha](layer_background_alpha)
-   [layer_background_index](layer_background_index)
-   [layer_background_speed](layer_background_speed)
-   [layer_background_xscale](layer_background_xscale)
-   [layer_background_yscale](layer_background_yscale)
-   [layer_background_get_visible](layer_background_get_visible)
-   [layer_background_get_sprite](layer_background_get_sprite)
-   [layer_background_get_htiled](layer_background_get_htiled)
-   [layer_background_get_vtiled](layer_background_get_vtiled)
-   [layer_background_get_stretch](layer_background_get_stretch)
-   [layer_background_get_blend](layer_background_get_blend)
-   [layer_background_get_alpha](layer_background_get_alpha)
-   [layer_background_get_index](layer_background_get_index)
-   [layer_background_get_speed](layer_background_get_speed)
-   [layer_background_get_xscale](layer_background_get_xscale)
-   [layer_background_get_yscale](layer_background_get_yscale)

Note that if you want to set the background position or the background
horizontal or vertical scrolling speed then you need to use the
following general layer functions:

-   [layer_x](../General_Layer_Functions/layer_x)
-   [layer_y](../General_Layer_Functions/layer_y)
-   [layer_hspeed](../General_Layer_Functions/layer_hspeed)
-   [layer_vspeed](../General_Layer_Functions/layer_vspeed)
