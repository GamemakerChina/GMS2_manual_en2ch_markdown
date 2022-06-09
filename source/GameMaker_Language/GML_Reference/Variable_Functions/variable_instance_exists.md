# variable_instance_exists

With this function you can check whether an instance scope variable
exists or not. You supply the unique instance ID value (which can be
found from the [Instance
Properties](../../../The_Asset_Editors/Room_Properties/Layer_Properties)
in the room editor, or is returned when you call the function [
instance_create_layer()
](../Asset_Management/Instances/instance_create_layer) ) as well as
the variable name to check for *as a string* (see example code below).
The function will return true if a variable with the given name exists
for the instance and false otherwise.

#### Syntax:

``` gml
variable_instance_exists(instance_id, name);
```

|             |                                                                                                                    |                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument    | Type                                                                                                               | Description                                  |
| instance_id |  [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The unique ID value of the instance to check |
| name        |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The name of the variable to check for        |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !variable_instance_exists(id, "shields")
{
    shields = 0;
}
```

The above code will check to see if the variable called "shields" exists
in the instance running the code and if it does not then it is created
and initialised to 0.
