# YUV Videos

Platforms that use the YUV colour format for videos require extra steps
for drawing those videos. This involves using a shader to draw two
surfaces on a primitive quad. Read the [video_draw()](video_draw)
reference page first for information on what data that function returns
for YUV videos, and then continue reading below for instructions on
using that data to draw the video.

## YUV Shader

Create a shader asset in your project, and replace its Fragment Shader (
.fsh ) code with this:

``` gml
//
// CUSTOM fragment shader for handling YUV content
//
varying vec2 v_vTexcoord;
varying vec4 v_vColour;
uniform sampler2D v_chroma;
const float x = 1.164383;
const float y = 1.138393;
const float z = 1.138393;
const vec3 src_bias = vec3(16.0 / 255.0, 128.0 / 255.0, 128.0 / 255.0);
const mat3 src_xform = mat3(1.00000000 * x,  0.00000000 * y,  1.57480000 * z,
1.00000000 * x, -0.18732427 * y, -0.46812427 * z,
            1.00000000 * x,  1.85560000 * y,  0.00000000 * z);
void main()
{
float yy = texture2D(gm_BaseTexture, vec2(v_vTexcoord.x, v_vTexcoord.y)).r;
vec2 cbcr = texture2D(v_chroma, vec2(v_vTexcoord.x, v_vTexcoord.y)).rg;
vec3 yuv = vec3(yy, cbcr);
yuv -= src_bias;
yuv *= src_xform;
gl_FragColor = vec4(yuv, 1.0);
}
```

## Get Sampler

In the Create event of your object, get the sampler ID of the v_chroma
shader uniform, only if the video is YUV:

``` gml
var _format = video_get_format();
if (_format == video_format_yuv)
{
videochromasampler = shader_get_sampler_index(shader_YUV, "v_chroma");
}
```

## Draw Video

In the Draw event of your object, call [video_draw()](video_draw) ,
and if its first array position is **0** (meaning the video is playing),
draw the video. In the code below, we're using a switch statement on the
[video_get_format()](video_get_format) function. If the video is
using the RGBA format, then it simply draws the surface in position
\[1\] of the array. If the video is using the YUV format, it uses the
shader to draw the two surfaces (in positions \[1\] and \[2\] ) onto a
primitive quad.

``` gml
var _data = video_draw();
if(_data[0] == 0)
{
    switch(video_get_format())
    {
        case video_format_rgba:
            var _surf = _data[1];
            draw_surface(_surf,0,0);
        break;
    
        //  #### YUV PART HERE ####
        case video_format_yuv:
            var _surf = _data[1];
            var _chromasurf = _data[2];
            if(surface_exists(_surf) and surface_exists(_chromasurf))
            {
                shader_set(shader_YUV);
            
                var _tex_id = surface_get_texture(_surf);
                var _chroma_tex_id = surface_get_texture(_chromasurf);
                texture_set_stage(videochromasampler, _chroma_tex_id);
                gpu_set_texfilter(false);
            
                draw_primitive_begin_texture(pr_trianglestrip, _tex_id);
            draw_vertex_texture(0, 0, 0, 0);
                draw_vertex_texture(surface_get_width(_chromasurf), 0, 1, 0);
                draw_vertex_texture(0, surface_get_height(_chromasurf), 0, 1);
                draw_vertex_texture(surface_get_width(_chromasurf), surface_get_height(_chromasurf), 1, 1);
                draw_primitive_end();
            
                gpu_set_texfilter(true);
                shader_reset();
            }
        break;
    }
}
```

The code under case video_format_yuv: does the following:

-   Gets the video surface ( \_surf ) and the chroma surface (
    \_chromasurf )
-   Makes sure that they exist, using
    [surface_exist()](../Surfaces/surface_exists)
    -   Sets the shader to shader_YUV (which is our newly created YUV
        shader)
    -   Gets the textures of both surfaces
    -   Assigns the texture of the chroma surface to the sampler we
        retrieved in the Create event
    -   Disables texture filtering
    -   Begins drawing a triangle strip primitive, with the video
        surface's texture assigned to it
    -   Draws a rectangle to cover the video surface, uses the width and
        height of the chroma surface for that rectangle
    -   Ends the primitive
    -   Re-enables texture filtering and resets the shader

Here the main video surface is being drawn by the primitive, and the
chroma surface is being blended on to it by the shader. That is the
reason why the texture of the chroma surface was passed into the shader
via a sampler.
