# ds_stack_top

This function will *only* read the first value of the stack (that which
is "on top"). It will not *pop* the value, meaning that it can still be
read in the future by this function or the [ ds_stack_pop()
](ds_stack_pop) . If the stack is empty then the function will
return the constant undefined , otherwise it will return the real or
string value contained in the stack.

#### Syntax:

``` gml
ds_stack_top(id);
```

|          |                                                                                                                |                                            |
|----------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                           | Description                                |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to read from. |

#### Returns:

``` gml
 Variable

(Data type value that is stored in the stack) or

 undefined
```

#### Example:

``` gml
num = ds_stack_top(control_stack);
```

The above code will read the value from the stack indexed in the
variable "control_stack" and store the return value in the variable
"num".
