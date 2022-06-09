# matrix_stack_is_empty

This function can be used to check whether the matrix stack is empty
(returns true ) or not (returns false ).

#### Syntax:

``` gml
matrix_stack_is_empty();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !matrix_stack_is_empty()
{
    matrix_stack_clear();
}
```

The above code checks the matrix stack to see if it is empty and if it
is not it clears it.
