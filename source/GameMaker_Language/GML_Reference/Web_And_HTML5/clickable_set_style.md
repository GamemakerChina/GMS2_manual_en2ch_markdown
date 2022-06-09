# clickable_set_style

This function lets you set the CSS style properties for the given button
via the key/value pairs in the provided [ DS Map
](../Data_Structures/DS_Maps/DS_Maps) . You need to have previously
created the both the button element (using [ clickable_add()
](clickable_add) ) and the DS Map and supply the stored indices to
each as arguments.

#### Syntax:

``` gml
clickable_set_style(index, map)
```

|          |                                                                                                       |                                                  |
|----------|-------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                  | Description                                      |
| index    |  [Clickable ID](../../../../GameMaker_Language/GML_Reference/Web_And_HTML5/clickable_add)         | The index of the clickable icon to style.        |
| map      |  [DS Map ID](../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The index of the DS Map to set the style from.   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var map = ds_map_create();
ds_map_add(map, "opacity", "0.5");
clickable_set_style(button, map);
ds_map_destroy();
```

The above code will change the style of the clickable button with the
index stored in the variable "button".
