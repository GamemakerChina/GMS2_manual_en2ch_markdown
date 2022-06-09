# font_add_get_enable_aa

This function can be used to check whether anti-aliasing (AA) is enabled
for fonts added using [ font_add() ](font_add) . The function will
return true if AA is enabled, and false if it is not. Note that AA is
enabled by default, but you can change the AA state for added fonts
using the function [ font_add_enable_aa() ](font_add_enable_aa) , as
long as it is called *before* adding the font.

#### Syntax:

``` gml
font_add_get_enable_aa();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !font_add_get_enable_aa()
{
    font_add_enable_aa(true);
}
```

The above code checks the status of anti-aliasing for added fonts and if
it not enabled, then we enable it.
