# clickable_delete

This function must be used to remove a clickable icon previously created
with [ clickable_add() ](clickable_add) from the game window.

#### Syntax:

``` gml
clickable_delete(index);
```

|          |                                                                                                |                                        |
|----------|------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                           | Description                            |
| index    |  [Clickable ID](../../../../GameMaker_Language/GML_Reference/Web_And_HTML5/clickable_add)  | Index of the clickable icon to remove. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if clickable_exists(global.Help_Icon)
{
    clickable_delete(global.Help_Icon);
}
```

The above code removes the clickable icon indexed in the global variable
"Help_Icon" from the game window, if it exists.
