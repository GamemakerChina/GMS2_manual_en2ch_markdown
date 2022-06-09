# instance_id

This **read only** [array](../../../GML_Overview/Arrays) holds all
the [ id s](Instance_Variables/id) of every *active* instance within
the room. This means that if you have used any of the [Instance
Deactivate](Deactivating_Instances/Deactivating_Instances) functions
those instances that have been deactivated will not be included in this
array (if you have used a value from this array previously, it will now
return the keyword [noone](../../../GML_Overview/Instance_Keywords)
).

#### Syntax:

``` gml
instance_id[num];
```

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; instance_count; i ++;)
{
    with (instance_id[i]) speed += 0.1;
}
```

The above code will loop through all instances within the room and add
0.1 to their speed.
