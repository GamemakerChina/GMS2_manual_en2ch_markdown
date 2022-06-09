# matrix_stack_pop

This function removes the matrix that is at the top of the current
matrix stack.

#### Syntax:

``` gml
matrix_stack_pop();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var m1 = matrix_build(66, 145, 0, 0, 0, 0, 1, 1, 1);
var m2 = matrix_build(0, 0, 0, 0, 0, image_angle * 6, 1, 1, 1) ;
matrix_stack_push(m1);
matrix_stack_push(m2);
matrix_set(matrix_world, matrix_stack_top());
draw_sprite(spr_tyre, 0, 0, 0);
matrix_stack_pop();
matrix_stack_pop();
```

The above code will build two new matrices and then push them onto the
matrix stack. The world matrix is then set to the top of the stack, a
sprite is drawn and the transforms are then popped from the stack.
