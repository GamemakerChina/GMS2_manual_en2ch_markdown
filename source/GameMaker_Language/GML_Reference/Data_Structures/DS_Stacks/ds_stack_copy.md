# ds_stack_copy

This function can be used to copy the contents of one stack into
another. Note that this does *NOT* remove the contents from the original
stack, nor does it destroy the original stack. When using this function
the stack being copied to must have been previously created and if it
contained any items before the copy, then these will be cleared first
(meaning this information will be lost).

#### Syntax:

``` gml
ds_stack_copy(id, source);
```

|          |                                                                                                                |                                  |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                           | Description                      |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the new stack.         |
| source   |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The original stack to copy from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
with (instance_create_layer(x, y, "Enemies", obj_Enemy))
{
    stack = ds_stack_create();
    ds_stack_copy(stack, other.stack);
}
```

The above function creates a new instance and then in that instance it
creates a new DS stack and copies the contents of the stack in the
instance running the code block, into the newly created instance stack.
