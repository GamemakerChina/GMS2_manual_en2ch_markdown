# shaders_are_supported

This function will do a check to see if the chosen target platform
supports shaders, returning true if they do, and false if they do not.
It is important to note that on **Android** , if the project does not
have any shader resources defined, then the function will *always return
false * , regardless of whether the device supports shaders or not.

#### Syntax:

``` gml
shaders_are_supported();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
global.GFX = false;
if shaders_are_supported()
{
    if shader_is_compiled(sh_glass) &amp;amp;&amp;amp; shader_is_compiled(sh_warp)
    {
        global.GFX = true;
    }
}
```

The above code will set a global variable to false , and then if the
platform supports shaders and both the shaders being checked have
compiled correctly, it will be set to true .
