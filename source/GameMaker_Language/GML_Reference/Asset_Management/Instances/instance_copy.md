# instance_copy

With this function you can "clone" an instance as this will create a new
version of the instance running the code at its same position. The
"perf" argument is used to instruct this new instance to perform the
create event or not. This function returns the [ id
](Instance_Variables/id) of the new instance which can then be
stored in a variable or used to access that instance. **NOTE** : If you
choose not to perform the create event, you may encounter errors if the
instance depends on any variables initialised in this event.

#### Syntax:

``` gml
instance_copy(perf);
```

|          |                                                                            |                                                                           |
|----------|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                               |
| perf     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to perform the new instance's Create event (true) or not (false). |

#### Returns:

``` gml
 Instance ID
```

#### Example:

``` gml
var inst = instance_number(object_index);
if inst &amp;lt; 10
{
    instance_copy(true);
}
```

The above code creates a local variable and uses it to store the number
of instances of the object running the code in the room. If the number
is less than 10, the instance then makes a copy of itself.
