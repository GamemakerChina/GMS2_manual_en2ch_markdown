# Shader Constants

Apart from the shader functions and constants defined in the OpenGL ES
Shading Language (GLSL ES) [Reference
Pages](http://www.khronos.org/registry/gles/specs/2.0/GLSL_ES_Specification_1.0.17.pdf)
, there are also a number of shader constants available to you that are
unique to GameMaker . The following display matrix constants can be used
as array indices when using the shader array constant gm_Matrices :

|                                |                                                                                                                                                                                                                                                                                                                |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constant                       | Description                                                                                                                                                                                                                                                                                                    |
|  MATRIX_VIEW                   | This array index constant holds the index to the current view matrix. The index returned would be used as an array value when calling the gm_Matrices constant within the shader code.                                                                                                                         |
|  MATRIX_PROJECTION             | This array index constant holds the index to the current projection matrix. The index returned would be used as an array value when calling the gm_Matrices constant within the shader code.                                                                                                                   |
|  MATRIX_WORLD                  | This array index constant holds the index to the current world matrix. This can be used for things like lighting if you have light information in world-space. The index returned would be used as an array value when calling the gm_Matrices constant within the shader code.                                |
|  MATRIX_WORLD_VIEW             | This array index constant holds the index to the result of the world and view matrices multiplied together. This is often used for things like fog. The index returned would be used as an array value when calling the gm_Matrices constant within the shader code.                                           |
|  MATRIX_WORLD_VIEW_PROJECTION  | This array index constant holds the index to the result of the world, view and projection matrices multiplied together. This is the normal transformation matrix used for vertex positions. The index returned would be used as an array value when calling the gm_Matrices constant within the shader code.   |
|  MATRIX_MAX                    | This is not an array index, but rather returns the size of the matrix array in the vertex shader.                                                                                                                                                                                                              |
|  MAX_VS_LIGHTS                 | This is not an array index, but rather returns the number of the lights in the vertex shader.                                                                                                                                                                                                                  |

The following constant is also available for lighting:

|                 |                                                                            |
|-----------------|----------------------------------------------------------------------------|
| Constant        | Description                                                                |
|  MAX_VS_LIGHTS  | The maximum number of point and directional lights available in the shader |

The following pre-defined matrix uniforms and constants can be used in
your shader to access GameMaker specific values:

|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constant                | Description                                                                                                                                                                                                                              |
|  gm_Matrices\[matrix\]  | This array constant returns a transform matrix and is one of the available pre-defined uniforms that GameMaker creates for you to use within the shader code editor. The array index is chosen from one of the above listed constants.   |
|  gm_BaseTexture         | This is a 2D sampler constant that returns the texture of the current object, as set by GameMaker . So it would be the current sprite, surface or texture that would normally be used when drawing without the shader being called.      |
|  gm_LightingEnabled     | This can be used to get or set the GameMaker lighting when using 3D.                                                                                                                                                                     |
|  gm_FogStart            | This can be used to get the distance where polygons start to be blended with the fog colour.                                                                                                                                             |
|  gm_RcpFogRange         | This can be used to get the distance at which fog is maximal and nothing can be seen anymore.                                                                                                                                            |
|  gm_PS_FogEnabled       | This will return true or false if the GPU has pixel fog enabled or not.                                                                                                                                                                  |
|  gm_FogColour           | This can be used to get the fog colour used by GameMaker .                                                                                                                                                                               |
|  gm_VS_FogEnabled       | This will return true or false if the GPU has vertex fog enabled or not.                                                                                                                                                                 |
|  gm_AlphaTestEnabled    | This can be used to get alpha testing in the shader. See [ gpu_set_alphatestenable() ](../../Drawing/GPU_Control/gpu_set_alphatestenable) for more information on alpha testing.                                                     |
|  gm_AlphaRefValue       | This can be used to get the current alpha testing reference value. See [ gpu_set_alphatestref() ](../../Drawing/GPU_Control/gpu_set_alphatestref) for more information on the alpha test reference.                                  |
