# variable_instance_get

With this function you can get the value from a given named variable.
You supply the unique instance ID value (which can be found from the
[Instance
Properties](../../../The_Asset_Editors/Room_Properties/Layer_Properties)
in the room editor, or is returned when you call the function [
instance_create_layer()
](../Asset_Management/Instances/instance_create_layer) ) as well as
the name of the variable to get the value of *as a string* (see example
code below). The function will return the value held by the variable, or
undefined if the variable does not exist. **IMPORTANT!** If the variable
you are getting does not exist then the function will return the keyword
undefined and you may get errors that will stop the game from
functioning, so if in doubt use the function [ variable_instance_exists
](variable_instance_exists) first.

#### Syntax:

``` gml
variable_instance_get(instance_id, name);
```

|             |                                                                                                                    |                                               |
|-------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument    | Type                                                                                                               | Description                                   |
| instance_id |  [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The unique ID value of the instance to use    |
| name        |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The name of the variable to get (as a string) |

#### Returns:

``` gml
 Variable

(any data type) or

 undefined

(if the named variable does not exist)
```

#### Example:

``` gml
if variable_instance_exists(id, "shields")
{
    var ss = variable_instance_get(id, "shields");
}
else
{
    var ss = -1;
}
```

The above code will check to see if a variable exists and if it does
then the value it holds is retrieved and stored in a local variable. If
it does not exist, the local variable is set to -1.
