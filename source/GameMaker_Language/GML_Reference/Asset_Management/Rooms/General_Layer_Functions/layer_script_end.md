# layer_script_end

With this function you can assign a [script
function](../../../../GML_Overview/Script_Functions) to a layer and
it will be called after the layer is rendered. When adding a function to
a layer in this way, it will be run at the end of *each of the different
draw events* so you may want to check in the function assigned which
event is currently finished rendering and adapt the code to suit. This
can be done by checking the [ event_type
](../../Objects/Object_Events/event_type) and/or the [ event_number
](../../Objects/Object_Events/event_number) (see the extended
example below). Note that the function is *not* meant to be called in
any draw events or step events, but rather only needs to be called at
the start of the room in the **Room Creation Code** or in the **Create
Event** / **Room Start Event** of an instance.

#### Syntax:

``` gml
layer_script_end(layer_id, script)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| script   |  [Script Function](../../../../../../GameMaker_Language/GML_Overview/Script_Functions)                                                                                                                       | The script function index to assign to the layer                           |

#### Returns:

``` gml
N/A
```

#### Extended Example:

In this extended example, we will first show you how a simple script
function is structured to set some shader uniform data so that when the
given layer is drawn, this function will be run and the shader will work
correctly. In the example, it is worth noting how we check which event
is being called so that the rest of the function is only run on the
specific event that we require it to work on - in this case, only on the
main draw event:

``` gml
/// @function layer_shader_start();
function layer_shader_start()
{
    if event_type == ev_draw
    {
        if event_number == 0
        {
            colour_to_find = shader_get_uniform(sShaderDemo5, "f_Colour1");
            colour_to_set = shader_get_uniform(sShaderDemo5, "f_Colour2");
            shader_set(s_ColourChanger);
            shader_set_uniform_f(colour_to_find, 1,1,1 );
            shader_set_uniform_f(colour_to_set, 1,0,0 );
        }
    }
}
```

We would then have a companion function to reset the shader after all
the drawing is done:

``` gml
/// @function layer_shader_end();
function layer_shader_end()
{
    if event_type == ev_draw
    {
        if event_number == 0
        {
            shader_reset();
        }
    }
}
```

Now that we have defined our script functions for setting the shader, we
then have to assign them to a specific layer so that the layer knows to
call them. This would be done in the room creation code, or in the
create event or room start event of some controller object (they do not
need to be set every step, but rather once at the start of the room, or
when the layer is initially created):

``` gml
var lay_id = layer_get_id("Instances");
layer_script_begin(lay_id, layer_shader_start);
layer_script_end(lay_id, layer_shader_end);
```

This final code block assigns the scripts to the layer.
