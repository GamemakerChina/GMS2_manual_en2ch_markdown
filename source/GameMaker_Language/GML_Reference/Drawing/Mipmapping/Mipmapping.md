# Mipmapping

This section contains all the functions related to using the
[mipmapping](https://en.wikipedia.org/wiki/Mipmap) functions. Before
using these functions you should have enabled mipmapping for the
required texture pages in the [Texture Group
Editor](../../../../Settings/Texture_Groups) and/or enabled
mipmapping for those sprites that have been set to use only a single
texture page from the [General Game
Options](../../../../Settings/Game_Options) . The image below shows
the difference mipmapping can make when rendering your project:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/Mipmapping_Example.png)  
Once you have enabled mipmapping for the project or a texture page, you
can then use the following functions to get and set values which will
change how things will look in your project when run. The functions
listed below can be used to get the different values associated with
mipmapping in GameMaker :

-   [gpu_get_tex_mip_filter](gpu_get_tex_mip_filter)
-   [gpu_get_tex_mip_filter_ext](gpu_get_tex_mip_filter_ext)
-   [gpu_get_tex_mip_bias](gpu_get_tex_mip_bias)
-   [gpu_get_tex_mip_bias_ext](gpu_get_tex_mip_bias_ext)
-   [gpu_get_tex_min_mip](gpu_get_tex_min_mip)
-   [gpu_get_tex_min_mip_ext](gpu_get_tex_min_mip_ext)
-   [gpu_get_tex_max_mip](gpu_get_tex_max_mip)
-   [gpu_get_tex_max_mip_ext](gpu_get_tex_max_mip_ext)
-   [gpu_get_tex_max_aniso](gpu_get_tex_max_aniso)
-   [gpu_get_tex_max_aniso_ext](gpu_get_tex_max_aniso_ext)
-   [gpu_get_tex_mip_enable](gpu_get_tex_mip_enable)
-   [gpu_get_tex_mip_enable_ext](gpu_get_tex_mip_enable_ext)

The functions listed below can be used to set the different values
associated with mipmapping in GameMaker :

-   [gpu_set_tex_mip_filter](gpu_set_tex_mip_filter)
-   [gpu_set_tex_mip_filter_ext](gpu_set_tex_mip_filter_ext)
-   [gpu_set_tex_mip_bias](gpu_set_tex_mip_bias)
-   [gpu_set_tex_mip_bias_ext](gpu_set_tex_mip_bias_ext)
-   [gpu_set_tex_min_mip](gpu_set_tex_min_mip)
-   [gpu_set_tex_min_mip_ext](gpu_set_tex_min_mip_ext)
-   [gpu_set_tex_max_mip](gpu_set_tex_max_mip)
-   [gpu_set_tex_max_mip_ext](gpu_set_tex_max_mip_ext)
-   [gpu_set_tex_max_aniso](gpu_set_tex_max_aniso)
-   [gpu_set_tex_max_aniso_ext](gpu_set_tex_max_aniso_ext)
-   [gpu_set_tex_mip_enable](gpu_set_tex_mip_enable)
-   [gpu_set_tex_mip_enable_ext](gpu_set_tex_mip_enable_ext)
