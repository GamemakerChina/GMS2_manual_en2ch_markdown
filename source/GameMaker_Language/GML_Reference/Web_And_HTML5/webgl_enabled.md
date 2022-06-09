# webgl_enabled

This **read-only** variable will return whether WebGL is enabled ( true
) or not ( false ) for your game. It will only work for those games
running through a browser (ie: HTML5), and for all other platforms it
will return true.

#### Syntax:

``` gml
webgl_enabled
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if webgl_enabled
{
    global.quality = 1;
}
else global.quality = 0;
```

The above code checks the WebGL flag and then sets the global variable
"quality" accordingly.
