# Filters and Effects

## Filter/Effect Layers

In the Room Editor, you can add a new Filter/Effect layer by clicking on
the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_FX_Layer.png)  
button, which will add a new layer and open up its properties below:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Room_LayerFilterProperties.png)  
A Filter/Effect (or FX) layer is used to apply a visual filter or effect
to some layers. You can select an effect from the "Effect Type"
drop-down list, which will show you its parameters in the Layer
Properties window allowing you to modify how it looks and behaves. For
example, selecting the "Screen Shake" effect will allow you to change
its magnitude, shake speed and apply a sprite as its noise texture:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Room_LayerFilterParameters.png)  
Adding an FX layer will apply the selected effect to all other layers
that are *below* the FX layer, as demonstrated in this visual:  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Editor_Room_LayerFilterEffectOrder.png)  
This means that all "affected" layers will have the selected filter
applied to them (here, "Desaturate") as they are below an FX layer. Any
layers above the FX layer will be unaffected. A layer may be affected by
multiple effect layers that are present above it anywhere in the layer
order. To create filters/effects that are applied to only one layer,
see: [Single-Layer FX](#h) . NOTE Modifying the [depth of a
layer](../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_depth)
or [an
instance](../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/depth)
at runtime may change which FX layers are applied on it, by either
making its depth higher than an FX layer's depth (essentially going
*under* the FX layer and being affected) or making its depth lower than
an FX layer's depth (going *above* the FX layer and not being affected).

## Filter vs. Effect

A Filter only uses shaders and can be previewed in the Room Editor. An
Effect also has internal code for managing itself in addition to
shaders. Due to this, they can't be previewed in the Room Editor, and
only appear functional at runtime (in-game). For example, "
**Colourise** " is a Filter, where " **Windblown Particles** " is an
Effect.

## Effect Types

All the Filters and Effects in the **"Effect Type"** drop-down list are
documented on this page: [FX Types &
Parameters](FX/All_Filter_Effect_Types) .

## Single-Layer FX

While you can create an FX layer to apply a filter to multiple layers,
you are also able to assign a filter to one specific layer only, using
the [Inspector](../../IDE_Tools/The_Inspector) . Opening an
Inspector and selecting a room layer will allow you to apply a
filter/effect to it, and if that layer is a non-FX layer (e.g. Instance
Layer, Asset Layer, etc.) then the effect will only be applied to that
layer and not to any other layers below it.  
![](https://gms.magecorn.com/Manual/assets/Images/IDE%20Tools/Inspector_Room_Layers.png)  
You can also click on the  
![](https://gms.magecorn.com/Manual/assets/Images/Icons/Icon_Eye.png)  
icon to enable/disable the FX for the selected layer.

## Runtime Usage

You can add and control effects at runtime using the [Filter/Effect GML
Functions](../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/Filter_Effect_Functions)
. Please note that there are currently only two ways to ensure that
GameMaker loads a particular filter/effect in your game:

-   By adding the filter/effect in **at least one room** through the IDE
-   By calling
    [fx_create()](../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)
    with the filter/effect name as a string literal

This means that to use a specific filter/effect at runtime, it must have
either been added into a room first (so GameMaker knows you are going to
use it) or specified explicitly in an
[fx_create()](../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/fx_create)
call. Read [Filter and Effect
Functions](../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/Filter_Effect_Layers/Filter_Effect_Functions)
for more information.
