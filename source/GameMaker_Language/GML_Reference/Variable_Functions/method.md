# method

With this function you can bind an existing function (or method) to the
given instance or struct, creating a new [method
variable](../../GML_Overview/Method_Variables) that can be used
later. You supply the instance ID to use (an instance that is active in
the room, and not an object index) or a struct reference, as well as the
function ID (or method reference) that you want to bind. The function
will return a new method which can be called from the variable it is
assigned to (see the code example below). The returned method will be
"bound" to the given instance or struct, meaning it will always execute
in the scope of that instance/struct. You can bind built-in functions as
well as user defined functions/methods, and you can also supply
undefined as the instance/struct argument meaning that the current [
self ](../../GML_Overview/Instance_Keywords) scope will be used for
the binding.

#### Syntax:

``` gml
method(struct_ref_or_instance_id, func);
```

|                           |                                                                                                                                                                                           |                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Argument                  | Type                                                                                                                                                                                      | Description                                                                                       |
| struct_ref_or_instance_id |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs) or [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The unique reference or ID value of the struct or instance to use (can be self or undefined )     |
| func                      |  [Script Function](../../../../GameMaker_Language/GML_Overview/Script_Functions) or [Method](../../../../GameMaker_Language/GML_Overview/Method_Variables)                        | The ID of the function (or method reference) to use                                               |

#### Returns:

``` gml
 Method
```

#### Example:

``` gml
var _inst = instance_position(mouse_x, mouse_y, obj_Enemy);
if instance_exists(_inst)
{
    enemy_func = method(_inst, enemy_ai);
}
```

The above code will check if an enemy instance exists at the mouse's
position. If it does then the enemy_ai method is bound to the enemy
instance and returned as a new method variable "enemy_func" .
