# font_add_enable_aa

This function can be used to enable or disable anti-aliasing (AA) for
fonts added using [ font_add() ](font_add) . This function needs to
be called *before* you add any fonts and setting it to true will enable
AA, and setting it to false will disable it. By default AA is enabled.
Note that this will have no effect on fonts that have been added before
the function was called, and the function only needs to be called once
when the font is added, and not every draw/step that the font is being
used.

#### Syntax:

``` gml
font_add_enable_aa(enable);
```

|          |                                                                            |                                                                         |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                             |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to enable ( true ) or disable ( false ) AA for added fonts.     |

#### Returns:

``` gml
N/A
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
