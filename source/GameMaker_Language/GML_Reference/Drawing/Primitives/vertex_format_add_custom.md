# vertex_format_add_custom

This function permits you to use a custom data type for specific vertex
format attributes as part of the new vertex format being created. The
available values to use are defined by the data type constant that you
choose, listed below:

|                                                                                                                                |                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
|  [Vertex Data Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_add_custom)  |                                                     |
| Constant                                                                                                                       | Description                                         |
|  vertex_type_float1                                                                                                            | A single floating point value                       |
|  vertex_type_float2                                                                                                            | Two floating point values                           |
|  vertex_type_float3                                                                                                            | Three floating point values                         |
|  vertex_type_float4                                                                                                            | Four floating point values                          |
|  vertex_type_colour                                                                                                            | Four component values (r, g, b, a)                  |
|  vertex_type_ubyte4                                                                                                            | Four component unsigned byte values (from 0 to 255) |

The use that these constants will be put too also needs to be defined so
that the values can be "bound" properly within the shader being created.
This is necessary due to the fact that DX and OpenGL have different
requirements so if you don't bind them properly, they won't come through
right in the shader. The available usage constants that you can choose
are listed below and those you use will depend on the specifics of the
shader being created:

|                                                                                                                                 |                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
|  [Vertex Usage Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_add_custom)  |                                                                           |
| Constant                                                                                                                        | Description                                                               |
|  vertex_usage_position                                                                                                          | position values (x, y, z)                                                 |
|  vertex_usage_colour                                                                                                            | colour values (r, g, b, a)                                                |
|  vertex_usage_normal                                                                                                            | vertex normal values (nx, ny, nz)                                         |
|  vertex_usage_textcoord                                                                                                         | UV coordinates (u, v)                                                     |
|  vertex_usage_blendweight                                                                                                       | the blendweight of the input matrix (for skeletal animation, for example) |
|  vertex_usage_blendindices                                                                                                      | the indices of the matrices to use (for skeletal animation, for example)  |
|  vertex_usage_depth                                                                                                             | vertex depth buffer value                                                 |
|  vertex_usage_tangent                                                                                                           | tangent values                                                            |
|  vertex_usage_binormal                                                                                                          | binormal values                                                           |
|  vertex_usage_fog                                                                                                               | fog values                                                                |
|  vertex_usage_sample                                                                                                            | sampler index                                                             |

There are some important things to note when using custom formats like
these:

-   The vertex_format_add_custom() function only supports
    vertex_usage_position , vertex_usage_colour , vertex_usage_normal
    and vertex_usage_textcoord when using GLSL shaders. These will map
    to the shader attributes in_Position , in_Colour\[0 - ...\] ,
    in_Normal respectively (anything that is not one of these three
    attributes - eg: texture coordinates - can be mapped to any
    attribute you define).
-   In general you should use vertex_usage_textcoord for all extra
    parameters where possible, as types like vertex_usage_blendweight
    and vertex_usage_tangent are close to deprecated in most shader
    languages, and probably won't convert properly. Instead use vec ,
    vec2 , vec3 or vec4 types vertex_usage_textcoord and everything
    should work fine.
-   GLSL ES does *not* support integer attributes, so passing in ivec4
    's does not work (this type is usually used when passing in
    vertex_usage_blendindices ). What you need to do is pass in texture
    coordinates and then in the shader, convert them to ivec4 like this:

``` gml
attribute vec3 in_Position;
attribute vec4 in_BlendIndices;
attribute vec4 in_BlendWeights;

varying vec4 v_vColour;
varying mat4 v_mat;

void main()
{
    gl_Position = gm_Matrices[MATRIX_WORLD_VIEW_PROJECTION] * vec4( in_Position.xyz, 1.0);
    v_vColour = in_BlendWeights;
     ivec4 t = ivec4(in_BlendIndices);
     v_mat = gm_Matrices[ t.x ];
}
```

-   Blend weights are usually stored in an array and then accessed using
    blend indices, but you can see here that instead of defining
    in_BlendIndices as an ivec4 attribute, it's a vec4 , then cast to an
    ivec4 in the code. This is then used to index the array created
    using the gm_Matrix (you can only access an array using an INT
    value - not a float).

#### Syntax:

``` gml
vertex_format_add_custom(type, usage);
```

|          |                                                                                                                                 |                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                            | Description                                                                                       |
| type     |  [Vertex Data Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_add_custom)   | The data type that this custom vertex data will hold (see the ***type constants*** listed above). |
| usage    |  [Vertex Usage Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_format_add_custom)  | The use that the data will get(see the ***usage constants*** listed above).                       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_format_begin();
vertex_format_add_textcoord();
vertex_format_add_custom(vertex_type_float3, vertex_usage_position);
my_format = vertex_format_end();
```

The above code will create a new vertex format with just texture and 3
custom floating point values for position. It is then stores the format
id in the variable "my_format".
