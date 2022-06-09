# instance_count

With this **read only** variable you can get a count of all active
instances that are in the room. This will include the instance running
the code, but does *not* include those instances that have been
deactivated using the [instance
deactivate](Deactivating_Instances/Deactivating_Instances)
functions. Note that this variable will only give you the number of
instances at the *start* of the step, so any changes to the instances in
the room made after the step has started will not be taken into
consideration.

#### Syntax:

``` gml
instance_count;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (instance_count &amp;lt; 100)
{
    var dif = 100 - instance_count;
    while (--dif &amp;gt; 0)
    {
        instance_create_layer(random(room_width), random(room_height), "Effects", obj_Star);
    }
}
```

The above code will create multiple instances of the object "obj_Star"
until the total instance count reaches 100.
