# external_free

This function frees the memory associated with the dll or dylib with the
given name. This should be done whenever the file in question is no
longer needed in the game, normally (for example) in a Game End event.

#### Syntax:

``` gml
external_free(id);
```

|          |                                                                                                         |                                                        |
|----------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                                                    | Description                                            |
| id       |  [External Function](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/external_define)  | The name of the dll or dylib that you want to free     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
external_free("MyDLL.dll");
```

The above example code will free the memory associated with the given
dll.
