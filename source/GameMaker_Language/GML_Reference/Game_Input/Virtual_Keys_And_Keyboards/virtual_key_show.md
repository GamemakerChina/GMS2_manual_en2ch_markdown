# virtual_key_show

Once you have created your virtual key for your devices, you may need to
debug and test that it is correctly positioned and working properly. For
that you would call this function, using the index of the virtual key
that you want to see (previously created and stored using [
virtual_key_add() ](virtual_key_add) ) which will draw a coloured
rectangle to represent the key on the screen. Once you are happy with
things it is recommended that you create and place your own graphic in
its area. ** NOTE ** The rectangle being drawn will be affected by the
blending, colour and alpha options set by the corresponding [draw
functions](../../Drawing/Colour_And_Alpha/Colour_And_Alpha) .

#### Syntax

``` gml
virtual_key_show(index);
```

|          |                                                                                                                               |                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                                                                          | Description                           |
| index    |  [Virtual Key ID](../../../../../GameMaker_Language/GML_Reference/Game_Input/Virtual_Keys_And_Keyboards/virtual_key_add)  | The index of the virtual key to show. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if global.Debug
{
    virtual_key_show(global.Left);
}
else
{
    virtual_key_hide(global.Left);
}
```

The above code checks the global variable "global.Debug" and if it tests
true then the virtual key indexed in the variable "global.Left" will be
drawn on the screen, and if it is false then the key will be hidden.
