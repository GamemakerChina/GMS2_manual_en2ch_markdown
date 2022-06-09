# time_source_get_parent

This function returns the [Time Source
ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)
of the given Time Source 's parent. The returned value may be the ID of
a custom Time Source , or one of the [Built-In Time
Sources](Built_In_Time_Sources) , depending on how the given Time
Source was [created](time_source_create) .

#### Syntax:

``` gml
time_source_get_parent(id);
```

|          |                                                                                                      |                                        |
|----------|------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                 | Description                            |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to get the parent of   |

#### Returns:

``` gml
 Time Source ID
```

#### Example:

``` gml
var _parent = time_source_get_parent(time_source);
```

This code gets the parent of a Time Source and stores it in a local
variable.
