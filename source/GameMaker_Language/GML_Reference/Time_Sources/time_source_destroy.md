# time_source_destroy

This function will destroy the given Time Source . You cannot destroy a
Time Source if it has existing [children](time_source_get_children)
. Destroy the child Time Source s first before destroying a parent (
[example](time_source_get_children) ).

#### Syntax:

``` gml
time_source_destroy(id);
```

|          |                                                                                                      |                              |
|----------|------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                 | Description                  |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to destroy   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
// Create event
time_source = time_source_create(time_source_game, 1, time_source_units_seconds, my_method, [], -1);

// Clean Up event
time_source_destroy(time_source);
```

The Create event code creates a new Time Source that expires once per
second and repeats indefinitely. The Clean Up event code destroys that
Time Source , as it will not be needed after the instance is destroyed.
