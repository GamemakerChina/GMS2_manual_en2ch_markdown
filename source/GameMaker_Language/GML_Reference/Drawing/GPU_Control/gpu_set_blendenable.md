# gpu_set_blendenable

This function can be used to toggle alpha-blending on and off.
Basically, if you have this set to false , all images being drawn will
be drawn 100% opaque, meaning that any transparent, or semi transparent,
areas of a sprite or background will be visible as a solid colour. It is
a good idea to have alpha blending *off* whenever possible (especially
when developing for mobile devices) as this greatly increases the draw
speed.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/Alphablend_Image.png)  

#### Syntax:

``` gml
gpu_set_blendenable(enable);
```

|          |                                                                            |                                                               |
|----------|----------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                   |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable or disable alpha blending value ( true or false ).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
gpu_set_blendenable(false); draw_sprite(spr_Background, 0, 0, 0); gpu_set_blendenable(true);
```

The above code switches off alpha blending to draw a background sprite
and then switches it back on again to continue drawing.
