# gc_enable

With this function you can enable or disable the garbage collector.
Calling the function with true as the argument enables it and using
false disables it (not recommended). It is enabled by default.

#### Syntax:

``` gml
gc_enable(enable);
```

|          |                                                                         |                                                                 |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                     |
| enable   |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  | enable ( true ) or disable ( false ) the garbage collector.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.debug == true)
{
    gc_enable(false);
}
```

The above code disables garbage collection if the given global variable
is true .
