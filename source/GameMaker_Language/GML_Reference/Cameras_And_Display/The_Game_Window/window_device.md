# window_device  DEPRECATED 

This function will return the current d3d device *pointer* , which you
can then (for example) pass through to a DLL or Dylib on Windows and
macOS. NOTE This function has been deprecated in GameMaker in favour of
[ os_get_info() ](../../OS_And_Compiler/os_get_info) .

#### Syntax:

``` gml
window_device();
```

#### Returns:

``` gml
 Pointer
```

#### Example:

``` gml
gfx_pointer = window_device();
```

The above code will store the d3d device pointer in a variable.
