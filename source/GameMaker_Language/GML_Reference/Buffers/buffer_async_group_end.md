# buffer_async_group_end

This function finishes the definition of a buffer async group. You must
have previously called the function [ buffer_async_group_begin()
](buffer_async_group_begin) to initiate the group, then call the
function [ buffer_save_async() ](buffer_save_async) for each file
that you wish to save out (or
[buffer_load_async()](buffer_load_async) to load buffers). Finally
you call this function, which will start the saving of the files. The
function will return a unique ID value for the save, which can then be
used in the [Asynchronous Save / Load
event](../../../The_Asset_Editors/Object_Properties/Async_Events/Save_Load)
to parse the results from the
[async_load](../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map.

#### Syntax:

``` gml
buffer_async_group_end();
```

#### Returns:

``` gml
 Async Request ID
```

#### Extended Example:

The buffer_async_group_end() function can be called from any event, and
since it is asynchronous the callback can be almost instantaneous or
could take several seconds. Calling the function is simple and would
look something like this:

``` gml
buffer_async_group_begin("SaveGame");
save1 = buffer_save_async(buff1, "Player_Save1.sav", 0, 16384);
save2 = buffer_save_async(buff2, "Player_Save2.sav", 0, 16384);
save3 = buffer_save_async(buff3, "Player_Save3.sav", 0, 16384);
save4 = buffer_save_async(buff4, "Player_Save4.sav", 0, 16384);
save_id = buffer_async_group_end();
```

The above code starts a buffer group then sets it to save out 4 files
asynchronously. The group definition is then ended (at which point
saving will begin), storing the ID of the function call in the variable
" *save_id* ". When the save is complete, the asynchronous Save/Load
event will be triggered and you can parse the async_load map for the
correct ID of the function, like this:

``` gml
if ds_map_find_value(async_load, "id") == saveid
{
    if ds_map_find_value(async_load, "status") == false
    {
        show_debug_message("Save failed!");
    }
}
```

The above code will first check the id of the DS map that has been
created, then check the status of the callback, posting a debug message
if there has been any issues.
