# variable_instance_set

With this function you can set the value of a given variable in an
instance. You supply the unique instance ID value (which can be found
from the [Instance
Properties](../../../The_Asset_Editors/Room_Properties/Layer_Properties)
in the room editor, or is returned when you call the function [
instance_create_layer()
](../Asset_Management/Instances/instance_create_layer) ) as well as
the name of the variable to set the value of *as a string* (see example
code below), and then finally the value to set (can be any valid [data
type](../../GML_Overview/Data_Types) ). If the variable does not
exist already in the instance it will be created and then assigned the
value.

#### Syntax:

``` gml
variable_instance_set(instance_id, name, val);
```

|             |                                                                                                                    |                                               |
|-------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument    | Type                                                                                                               | Description                                   |
| instance_id |  [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The unique ID value of the instance to use    |
| name        |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The name of the variable to set (as a string) |
| val         |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                                   | The value to set the variable to              |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !variable_instance_exists(id, "shields")
{
    variable_instance_set(id, "shields", 0);
}
```

The above code will check to see if an instance variable exists in the
calling instance and if it does not then it is created and set to 0.
