# ds_stack_size

This function will return the "size" of the stack, ie: the number of
items that have been pushed onto it.

#### Syntax:

``` gml
ds_stack_size(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if !ds_stack_empty(control_stack)
{
    num = ds_stack_size(control_stack);
}
```

The above code checks a DS stack to see if it is empty or not, and if it
is not, it gets the number of items that it contains and stores the
value in a variable.
