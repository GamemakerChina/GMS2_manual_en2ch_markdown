# ds_stack_push

This function will *push* (add) a value, which can be of any data type,
onto the top of the stack. The function can take a further 14 optional
arguments (making a total of 15 possible additions), permitting you to
push multiple values consecutively to the stack in a single call.

#### Syntax:

``` gml
ds_stack_push(id, val [, val2, ... val15]);
```

|                     |                                                                                                                |                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument            | Type                                                                                                           | Description                                |
| id                  |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to push onto. |
| val                 |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                            | The value to push onto the stack.          |
| \[val2, ... val13\] |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                            | Optional values to be added to the stack.  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
move_stack = ds_stack_create(); ds_stack_push(move_stack, x, y, x, y + 200, x + 200, y + 200, x +200, y);
```

The above code creates a new DS stack and stores its index in the
variable "move_stack". It then pushes a number of values onto the stack
for future use.
