# buffer_async_group_begin

This function is called when you want to begin the saving out of
multiple buffers to multiple files (or loading multiple buffers). The
groupname is a string and will be used as the directory name for where
the files are saved, and should be used as part of the file path when
loading the files back into the IDE later (using any of the [
buffer_load() ](buffer_load) functions). This function is *only* for
use with the [ buffer_save_async() ](buffer_save_async) and
[buffer_load_async()](buffer_load_async) functions and you must also
end the async group by calling [ buffer_async_group_end()
](buffer_async_group_end) function otherwise the files will not be
saved/loaded. Note that for the console platforms (like PS4 for
example), the groupname will be used as the save slot description, and
using this function can help you avoid having the UI show for every file
that is being saved out. Also note that when using UWP you can roam your
save games between native Xbox and Microsoft store windows by creating a
group that is the same as an ERA Xbox group, for example:

``` gml
if os_type == os_uwp
{
    buffer_async_group_begin("root/yourgroupname");
}
else
{
    buffer_async_group_begin("yourgroupname");
}
```

#### Syntax:

``` gml
buffer_async_group_begin(groupname);
```

|           |                                                                        |                                      |
|-----------|------------------------------------------------------------------------|--------------------------------------|
| Argument  | Type                                                                   | Description                          |
| groupname |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the group (as a string). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_async_group_begin("SaveGame");
save1 = buffer_save_async(buff1, "Player_Save1.sav", 0, 16384);
save2 = buffer_save_async(buff2, "Player_Save2.sav", 0, 16384);
save3 = buffer_save_async(buff3, "Player_Save3.sav", 0, 16384);
save4 = buffer_save_async(buff4, "Player_Save4.sav", 0, 16384);
buffer_async_group_end();
```

The above code starts a buffer group then sets it to save out 4 files
asynchronously. The group definition is then ended (at which point
saving will begin).
