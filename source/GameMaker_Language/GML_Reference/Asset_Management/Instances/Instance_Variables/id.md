# id

This **read-only** variable holds the unique identifying number for the
instance. Every instance that you create - whether through code or by
adding them to a room in the Room Editor - is given a number that is
used internally to identify this instance and the variable id is what
you can use to reference it. The id is also returned (and can be stored
in a variable) when an instance is created using
[instance_create_layer()](../instance_create_layer) or
[instance_create_depth()](../instance_create_depth) , as well as
other instance functions. NOTE The value of this variable is *not* the
same as the identifier that the instance is given in the room editor and
is also different to the [ instance_id ](../instance_id) array which
contains all the ids of all the currently active instances.

#### Syntax:

``` gml
id;
```

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; instance_count; i++;)
{
    if instance_id[i] != id
    {
        instance_id[i].scr += 5;
    }
}
```

The above code adds 5 to the "scr" variable for every active instance in
the room except the one running the code. It does this by looping
through ALL the active instances (using the "instance_id" array to
return each active instances ID) and comparing them against the built in
"id" variable, which is the ID of the original instance running the
code.
