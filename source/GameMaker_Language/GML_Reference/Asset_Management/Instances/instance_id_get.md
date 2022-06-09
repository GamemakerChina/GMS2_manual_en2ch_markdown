# instance_id_get

With this function you can get the unique ID value of any instance from
the currently active instance list. You give the index in the instance
list to get the ID from and the function will return the value for
storing in a variable.

#### Syntax:

``` gml
instance_id_get(index);
```

|          |                                                                         |                                                                       |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                           |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index within the instance list from 0 to instance count - 1 .     |

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; instance_count; ++i;)
{
    var temp_id = instance_id_get(i);
    with (temp_id)
    {
        speed += 0.1;
    }
}
```

The above code will loop through all instances within the room and add
0.1 to their speed.
