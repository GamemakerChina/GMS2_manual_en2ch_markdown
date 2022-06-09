# virtual_key_delete

If your game has different rooms or instances to control menus and
game-play and other things, then it is probable that you will need to
change the position and key maps of your virtual keys at some point. For
that you can use this function to delete the old ones before creating
the new ones (if necessary). The function requires that you supply the
ID of the virtual key to delete - as returned by [ virtual_key_add()
](virtual_key_add) . Note that any virtual keys will be
automatically removed from the room when the room is changed, so this
function is *only* necessary when you wish to manually remove the keys
before the room itself has finished.

#### Syntax

``` gml
virtual_key_delete(index);
```

|          |                                                                                                                               |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                          | Description                             |
| index    |  [Virtual Key ID](../../../../../GameMaker_Language/GML_Reference/Game_Input/Virtual_Keys_And_Keyboards/virtual_key_add)  | The index of the virtual key to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
virtual_key_delete(global.Left);
```

The above code deletes the virtual key indexed in the global variable
"global.Left".
