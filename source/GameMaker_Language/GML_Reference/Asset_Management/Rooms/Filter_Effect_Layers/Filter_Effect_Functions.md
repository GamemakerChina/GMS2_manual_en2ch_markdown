# Filter and Effect Functions

## Overview

There are various GML functions that can be used to create, modify and
remove filters/effects from layers within a room, allowing you to easily
manage effects in real-time to create realistic and dynamic
filters/effects. Please note that there are currently only two ways to
ensure that GameMaker loads a particular filter/effect in your game:

-   By adding the filter/effect in **at least one room** through the IDE
-   By calling [fx_create()](fx_create) with the filter/effect name
    as a string literal

This means that to use a specific filter/effect at runtime, it must have
either been added into a room first (so GameMaker knows you are going to
use it) or specified explicitly in an [fx_create()](fx_create) call.
The latter method (of specifying the filter/effect in your code) only
works with string literal s directly specified in the function argument,
which means that if you use a variable or any logic to come up with the
filter/effect name string, then the asset compiler will not detect that
and the filter/effect will not be loaded. Consider the following
examples:

``` gml
// This will work on its own
var _fxshake = fx_create("_filter_screenshake");

// This will NOT work on its own
var _myfilters = { screenshake: "_screenshake" }
var _filter_to_use = "_filter" + _myfilters.screenshake;
var _fxshake = fx_create(_filter_to_use);
```

To ensure that the latter method works, you can simply add the filter to
at least one room in your project, or ensure that
[fx_create()](fx_create) is called anywhere in your project with the
filter name as a string constant (and not a variable).

## Function List

The following functions are used to create and manage "FX Structs"
containing effect data:

-   [fx_create](fx_create)
-   [fx_get_parameter](fx_get_parameter)
-   [fx_get_parameters](fx_get_parameters)
-   [fx_get_name](fx_get_name)
-   [fx_get_parameter_names](fx_get_parameter_names)
-   [fx_get_single_layer](fx_get_single_layer)
-   [fx_set_parameter](fx_set_parameter)
-   [fx_set_parameters](fx_set_parameters)
-   [fx_set_single_layer](fx_set_single_layer)

The following functions are used for modifying layers that may contain
Filters/Effects by making use of FX Structs:

-   [layer_set_fx](layer_set_fx)
-   [layer_get_fx](layer_get_fx)
-   [layer_clear_fx](layer_clear_fx)
-   [layer_enable_fx](layer_enable_fx)
-   [layer_fx_is_enabled](layer_fx_is_enabled)

## Modify FX At Runtime

You can modify filters/effects at runtime by doing the following:

-   **Retrieve the FX struct** from the layer you want to modify by
    calling [layer_get_fx()](layer_get_fx)
    -   *Or, create a new FX struct by calling
        [fx_create()](fx_create) and apply it to a layer using
        [layer_set_fx()](layer_set_fx) *
-   **Retrieve its parameter struct** by calling
    [fx_get_parameters()](fx_get_parameters)
-   **Modify the parameters** as required by assigning values to the
    struct variables
    -   *Get the parameter names from here: [FX Types &
        Parameters](../../../../../The_Asset_Editors/Room_Properties/FX/All_Filter_Effect_Types)*
-   **Apply the modified struct** back to the FX struct by calling
    [fx_set_parameters()](fx_set_parameters)
    -   *You do not need to call [ layer_set_fx() ](layer_set_fx)
        here as modifying the FX struct directly affects the layer it is
        already assigned to*

Here is example code for the workflow mentioned above: Create Event

``` gml
// Store the FX struct, and its parameters struct, in variables
pixelate_fx = layer_get_fx("Effect_1");
pixelate_fx_params = fx_get_parameters(pixelate_fx);
```

Step Event

``` gml
// Change param as variable
pixelate_fx_params.g_CellSize = round((mouse_x / room_width) * 64);

// Or, change param as string
pixelate_fx_params[$ "g_CellSize"] = round((mouse_x / room_width) * 64);

// Apply updated parameters struct to the FX struct
fx_set_parameters(pixelate_fx, pixelate_fx_params);
```

## FX Runtime Parameters

The [FX Types &
Parameters](../../../../../The_Asset_Editors/Room_Properties/FX/All_Filter_Effect_Types)
page lists all Filters/Effects along with their **Runtime Parameters** .
You can use the Runtime parameter names in the following three ways
(using the parameter "g_CellSize" as an example):

-   Modify a parameter in an FX struct by calling
    [fx_set_parameter()](fx_set_parameter) :
    fx_set_parameter(fx_struct, **"g_CellSize"** , 8);
-   Modify a variable in a parameter struct: params_struct.
    **g_CellSize** = 8;
    -    NOTE *Make sure to get the parameter struct first by calling
        [fx_get_parameters()](fx_get_parameters) .*
-   Modify a variable in a parameter struct using the $ accessor and a
    string: params_struct\[$ **"g_CellSize"** \] = 8;

## Single Layer Mode

By default, a filter/effect is applied to the layer that it is [assigned
to](layer_set_fx) and all layers below that layer, however you can
use [ fx_set_single_layer() ](fx_set_single_layer) to enable
**Single Layer** mode for a filter/effect to make sure that it's only
applied to the layer that it is assigned to. The following visual shows
a filter being applied to multiple layers (which is the default
behaviour for all FX layers), and then the same filter with Single Layer
mode enabled and applied to a non-FX layer:

![Single Layer Mode
OFF](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/FX_single_layer_off.png)

![Single Layer Mode
ON](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Rooms/FX_single_layer_on.png)

You can also make use of Single-Layer effects in the Room Editor by
using the [Inspector](../../../../../IDE_Tools/The_Inspector) .
