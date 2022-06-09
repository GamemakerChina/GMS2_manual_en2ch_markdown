# Shaders

Shaders are an incredibly powerful tool for manipulating what and how
things are rendered to the screen by the graphics card. Since these tiny
programs are actually run on the graphics card itself, this means that
they are extremely fast to process, freeing up valuable CPU cycles for
more game logic. To create a shader you will need to have written both a
**Vertex Shader** and a **Fragment Shader** (also know as a **Pixel
Shader** ) using the [Shader
Editor](../../../../The_Asset_Editors/Shaders) , and even if (for
example) you only wish to change the vertex positions for an instance
being drawn, or if you only want to change the colour values for the
pixels, you will still need **both** programs for a complete shader to
work. NOTE Shaders do **not** permit you to change the value of any
variables that you pass into them, and so these will be called **shader
constants** in all the documentation that refers to them. For a complete
overview of the available GLSL ES functions and variables that you can
use to program the shaders themselves, please refer to the [OpenGL ES
Shading Language (GLSL ES) Reference
Pages](https://www.khronos.org/registry/OpenGL/specs/es/2.0/es_cm_spec_2.0.pdf)
. The following link is also useful as it contains some quick reference
cards for the OpenGL ES API (note that only the last two cards shown are
applicable to GameMaker ): [OpenGL ES Reference
Cards](https://www.khronos.org/opengles/sdk/docs/reference_cards/OpenGL-ES-2_0-Reference-card.pdf)
. Using a shader in your projects is very simple, and only requires a
couple of lines of code to get the most basic of use from it:

``` gml
shader_set(myShader);
draw_self();
shader_reset();
```

As you can see, they are used in a similar manner to blend modes and
surfaces, where you first select (set) the shader, draw what you want
using it, then reset the draw target again afterwards. If you wish to
render the full screen through a shader, and not just a single sprite or
background, you will need to set up a surface to catch the current view,
and then pass that through to the shader (see
[Surfaces](../../Drawing/Surfaces/Surfaces) for more information).
**NOTE** : Shaders, like anything related to drawing, can **only be used
in the draw event** . It is also worth noting that if you are trying to
use a colour value in a shader and the object has no texture, the
results will turn out black. If the shader you are using has input
values, these are set using the *uniform* functions. You would first get
the uniform *handle* (which is essentially an ID value for the uniform
to be set) using the function [ shader_get_uniform()
](shader_get_uniform) in the **Create Event** of the instance using
the shader, and then store these handles in variables, something like
this:

``` gml
colour_to_find = shader_get_uniform(sShaderDemo5, "f_Colour1");
colour_to_set = shader_get_uniform(sShaderDemo5, "f_Colour2");
```

Once you have the uniform handles, they can then be set in the shader
code for the **Draw Event** like this:

``` gml
shader_set(sShaderDemo5);
shader_set_uniform_f(colour_to_find, 1,1,1 );
shader_set_uniform_f(colour_to_set, 1,0,0 );
draw_sprite(sprite_index,image_index,x+24, y);
shader_reset();
```

One final thing to note is that although shaders are accepted across all
platforms, they are still device specific and if the hardware or
software of the device cannot use shaders then you will get an error.
Therefore you are recommended to check that the shader has been compiled
before setting uniforms or using the shader itself, like this:

``` gml
if (shader_is_compiled(myShader))
{
    shader_set(myShader);
    draw_self();
    shader_reset();
}
else show_debug_message("Shader failed");
```

As an extra check you can also call the function [
shaders_are_supported() ](shaders_are_supported) to see if the
hardware even supports shaders. In general you'd do these checks on game
start and store the results as a [global
variable](../../../GML_Overview/Variables/Global_Variables) to then
check later. It is important to note that GameMaker also supports some
conditional compile **Macros** which can be used within GLSL ES shaders
so they can perform alternative code on specific supported platforms.
The macros and the platforms they will be generated on are shown in the
table below:

|               |       |                        |
|---------------|-------|------------------------|
| Shader Macro  | Value | Target Platform        |
| \_YY_GLSLES\_ | 1     | All target platforms   |
| \_YY_GLSL\_   | 2     | Mac and Ubuntu (Linux) |
| \_YY_HLSL11\_ | 3     | Windows, UWP, XboxOne  |
| \_YY_PSSL\_   | 4     | PS4                    |

When you compile your GameMaker project on any one of the listed
platforms using a GLSL ES format shader, *one* of the above macros will
be generated which can then be used checked in the shader code like
this:

``` gml
#ifdef _YY_HLSL11_
// HLSL shader code here
#else
// GLSL shader code here
#endif
```

If you are new to shaders or want a more complete guide to creating and
use them using GameMaker , then please see the following page of the
manual:

-   [Guide To Using
    Shaders](../../../../Additional_Information/Guide_To_Using_Shaders)

The following functions are available for drawing and setting shaders:

-   [shader_get_name](shader_get_name)
-   [shader_get_uniform](shader_get_uniform)
-   [shader_get_sampler_index](shader_get_sampler_index)
-   [shader_set](shader_set)
-   [shader_set_uniform_f](shader_set_uniform_f)
-   [shader_set_uniform_f\_array](shader_set_uniform_f_array)
-   [shader_set_uniform_i](shader_set_uniform_i)
-   [shader_set_uniform_i\_array](shader_set_uniform_i_array)
-   [shader_set_uniform_matrix](shader_set_uniform_matrix)
-   [shader_set_uniform_matrix_array](shader_set_uniform_matrix_array)
-   [shader_reset](shader_reset)
-   [shader_is_compiled](shader_is_compiled)
-   [shaders_are_supported](shaders_are_supported)
-   [shader_current](shader_current)

We also have a special function which defines a global state for all
shaders:

-   [shader_enable_corner_id](shader_enable_corner_id)

When working with texture samplers in shaders you will need information
about the texture being used, in which case you can use the following
functions:

-   [sprite_get_texture](../Sprites/Sprite_Information/sprite_get_texture)
-   [sprite_get_uvs](../Sprites/Sprite_Information/sprite_get_uvs)
-   [font_get_texture](../Fonts/font_get_texture)
-   [font_get_uvs](../Fonts/font_get_uvs)
-   [texture_get_width](../../Drawing/Textures/texture_get_width)
-   [texture_get_height](../../Drawing/Textures/texture_get_height)
-   [texture_get_texel_width](../../Drawing/Textures/texture_get_texel_width)
-   [texture_get_texel_height](../../Drawing/Textures/texture_get_texel_height)
-   [texture_set_stage](../../Drawing/Textures/texture_set_stage)
-   [gpu_set_texfilter_ext](../../Drawing/GPU_Control/gpu_set_texfilter_ext)
-   [gpu_set_texrepeat](../../Drawing/GPU_Control/gpu_set_texrepeat)

While this manual will **not** cover any of the Open GL shader functions
and variables, it does contain a list of the ones that are unique to
GameMaker . These constants are not part of the Open GL specification
for shaders and are supplied to simplify the integration of shaders
within your projects.

-   [Shader Constants](Shader_Constants)

Finally, GameMaker permits you to define your own **Vertex Formats**
from which you can create your own custom primitives. This can greatly
speed up shader operations or can be used to extend their capabilities
and create surprising effects. You can find information on this in the
following sections:

-   [Primitives And Vertex
    Formats](../../Drawing/Primitives/Primitives_And_Vertex_Formats)
