# ds_stack_pop

This function will *pop* the top value off of the DS stack, removing it
from the stack and returning the value to be stored in a variable. If
the stack is empty then the function will return the constant undefined
, otherwise it will return the real or string value contained in the
stack.

#### Syntax:

``` gml
ds_stack_pop(id);
```

|          |                                                                                                                |                                           |
|----------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                           | Description                               |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to pop from. |

#### Returns:

``` gml
 Variable

(Data type value that is stored in the stack) or

 undefined
```

#### Example:

``` gml
if !ds_stack_empty(move_stack)
{
    var xx = ds_stack_pop(move_stack);
    var yy = ds_stack_pop(move_stack);
    move_towards_point(xx, yy, 4);
}
```

The above code checks the DS stack indexed in the variable "move_stack"
to see if it is empty, and if it is not, it then pops the top two values
from the stack and use them to set a direction for movement.
