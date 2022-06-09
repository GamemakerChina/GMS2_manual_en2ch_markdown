# gpu_pop_state

This function pops the previous GPU state from the stack and applies it.
See [ gpu_push_state() ](gpu_push_state) for more information.

#### Syntax:

``` gml
gpu_pop_state();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
gpu_push_state();
gpu_set_blendmode(bm_add);
gpu_set_blendenable(false);
gpu_set_cullmode(true);
with (obj_Effect_Parent)
{
    draw_self();
}
gpu_pop_state();
```

The above code will "save" the current GPU state on the stack, then
change certain GPU settings and draw a group of instances before
resetting the GPU state to what it was previously.
