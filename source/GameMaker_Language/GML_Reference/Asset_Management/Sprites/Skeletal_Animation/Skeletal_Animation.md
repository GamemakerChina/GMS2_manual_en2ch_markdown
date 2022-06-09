# Skeletal Animation Sprites

The functions found in this section are *only* for use with sprites that
have been imported from a skeletal animation file (specifically, the
JSON files that [**Spine**](http://es.esotericsoftware.com/) exports)
and can be used to get information about an animation asset in your
game, as well as for setting certain properties within an animation.
These functions can to be used along with the regular sprite functions
and variables, permitting you to (for example) mix two skeleton
animations using these special functions while setting the image scale
using the normal sprite instance variables (for more information on the
sprite instance variables see
[here](../Sprite_Instance_Variables/Sprite_Instance_Variables) ).
NOTE For further information on importing skeletal animation sprites
made with Spine, please see the section [Importing Non-Bitmap
Sprites](../../../../../Settings/Texture_Information/Non-Bitmap_Sprites)
. You can find out more about the functions for these kinds of sprites
from the sections below:

-   [Animation](Animation/Animation)
-   [Skins](Skins/Skins)
-   [Attachments](Attachments/Attachments)
-   [Bones](Bones/Bones)
-   [Slots](Slots/Slots)
-   [Drawing and
    Miscellaneous](Drawing_And_Miscellaneous/Drawing_And_Miscellaneous)

## Tint Black Support

This feature allows the dark areas of Spine sprite slots to be tinted
differently to the light areas (this is a Spine IDE feature, see the
**Tint black** section
[here](http://esotericsoftware.com/spine-attachments) more details).
Currently, in order to make use of this feature in GameMaker , you are
required to use a custom
[shader](../../../../../The_Asset_Editors/Shaders) when drawing a
Spine sprite that uses it. This shader contains a global uniform
variable called " gm_SpineTintBlackColour " which the runner fills with
the current tint-black colour, retrieved from the Spine data
automatically. The shader required is shown below: The Vertex Shader
(this is the same as the default passthrough vertex shader)

``` gml
attribute vec3 in_Position; // (x,y,z)
attribute vec4 in_Colour; // (r,g,b,a)
attribute vec2 in_TextureCoord; // (u,v)

varying vec2 v_vTexcoord;
varying vec4 v_vColour;

void main()
{
    vec4 object_space_pos = vec4( in_Position.x, in_Position.y, in_Position.z, 1.0);
    gl_Position = gm_Matrices[MATRIX_WORLD_VIEW_PROJECTION] * object_space_pos;
    v_vColour = in_Colour;
    v_vTexcoord = in_TextureCoord;
}
```

The Fragment Shader:

``` gml
varying vec2 v_vTexcoord;
varying vec4 v_vColour;

uniform vec4 gm_SpineTintBlackColour; // This is the uniform containing the tint-black colour

void main()
{
    vec4 tb = gm_SpineTintBlackColour;
    vec4 texcol = texture2D( gm_BaseTexture, v_vTexcoord );
    vec4 outcol;
    outcol.rgb = v_vColour.rgb * texcol.rgb;
    outcol.rgb += tb.rgb * ((tb.a * (texcol.a - 1.0)) + (1.0 - texcol.rgb)); // This line performs the tint-    black blending logic
    outcol.a = v_vColour.a * texcol.a;
    gl_FragColor = outcol;
}
```

You would use this by first calling the shader, then drawing the sprite,
then resetting the shader, something like this:

``` gml
shader_set(shd_spine_tint_black);
draw_self();
shader_reset();
```
