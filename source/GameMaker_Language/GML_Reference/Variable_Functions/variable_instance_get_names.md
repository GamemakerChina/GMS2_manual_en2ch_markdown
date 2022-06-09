# variable_instance_get_names

With this function you can retrieve an array populated with the
**instance** variable names for an instance, or the **global** variables
for a game. When you pass in an instance ID value, each entry in the
array will be a string of the variable name that corresponds to an
[instance scope](../../GML_Overview/Variables_And_Variable_Scope)
variable that has been created in the instance. However if you pass in
the keyword global , each entry in the array will be a string of the
variable name that corresponds to an [global
scope](../../GML_Overview/Variables_And_Variable_Scope) variable.

#### Syntax:

``` gml
variable_instance_get_names(instance_id/global);
```

|                    |                                                                                                                                |                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument           | Type                                                                                                                           | Description                                                          |
| instance_id/global |  [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id) or global    | The unique ID value of the instance to check or the keyword global   |

#### Returns:

``` gml
 Array

(each entry is a string)
```

#### Example:

``` gml
var str = "";
var array = variable_instance_get_names(id);
show_debug_message("Variables for " + object_get_name(object_index) + string(id));
for (var i = 0; i &amp;lt; array_length(array); i++;)
{
    str = array[i] + ":" + string(variable_instance_get(id, array[i]));
    show_debug_message(str);
}
```

The above code will retrieve an array of all instance scope variables
for the instance running the code block and then display these along
with their values in the debug output.
