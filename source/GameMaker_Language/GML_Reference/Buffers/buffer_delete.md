# buffer_delete

With this function you can delete a buffer previously have created using
the function [ buffer_create() ](buffer_create) from memory,
releasing the resources used to create it and removing any data that it
may currently contain. **NOTE** : It's important to always remove any
dynamically created resources from memory when you no longer need them
to prevent memory leaks. ***IMPORTANT!*** When you create a buffer, the
index value used to identify it is an integer value starting at 0. These
indices are re-used by GameMaker, so a destroyed buffer index value may
be used by a newly created one afterwards, and we recommend that you set
any variable that holds a buffer index to -1 after having destroyed the
buffer.

#### Syntax:

``` gml
buffer_delete(buffer)
```

|          |                                                                                       |                                    |
|----------|---------------------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                                  | Description                        |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_delete(player_buffer); player_buffer = -1;
```

The above code will delete the previously created buffer with the id
stored in the variable "player_buffer" and then sets the variable to -1.
