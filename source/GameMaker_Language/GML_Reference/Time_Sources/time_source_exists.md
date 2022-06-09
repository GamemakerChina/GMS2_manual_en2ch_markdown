# time_source_exists

This function returns whether the given ID is a valid Time Source . If
the Time Source was [destroyed](time_source_destroy) , this will
return false , however if the Time Source was
[stopped](time_source_stop) or it merely expired, it will continue
to exist, meaning this function returns true .

#### Syntax:

``` gml
time_source_exists(id);
```

|          |                                                                                                      |                            |
|----------|------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                 | Description                |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to check   |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (time_source_exists(global.spawn_time_source))
{
    if (keyboard_check_pressed(vk_space))
    {
        time_source_destroy(global.spawn_time_source);
    }
}
```

This code checks if a Time Source exists. If it does, it checks if the
Space key was pressed. In that case, it destroys the Time Source .
