# gpu_push_state

With this function you can push the current GPU state onto a stack to be
used later. You would generally use this if you want to "save" the
current GPU state (things like blend mode, alpha writing, culling,
etc... will all be pushed to the stack), then draw something with
different settings, and then reset the GPU stack to what it was before
(by calling [ gpu_pop_state() ](gpu_pop_state) ).

#### Syntax:

``` gml
gpu_push_state();
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
