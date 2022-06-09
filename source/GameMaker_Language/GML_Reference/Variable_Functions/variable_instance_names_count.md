# variable_instance_names_count

With this function you can find the total number number of variables
defined for an instance. You supply the instance ID to check, and the
function will return an integer value for the number of variables
encountered, or (if no instance of the given ID exists) -1.

#### Syntax:

``` gml
variable_instance_names_count(instance_id);
```

|             |                                                                                                                    |                                               |
|-------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument    | Type                                                                                                               | Description                                   |
| instance_id |  [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The unique ID value of the instance to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _num = variable_instance_names_count(myinst);
show_debug_message("Instance Variables = " + string(_num));
```

The above code will retrieve the number of variables in the given
instance and show a debug message in the console output with that value.
