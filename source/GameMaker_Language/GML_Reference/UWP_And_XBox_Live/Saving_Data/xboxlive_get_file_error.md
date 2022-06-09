# xboxlive_get_file_error

This function will return a constant (shown below) to help debug why a
file function failed so that you can take appropriate action in your
game code. When one of the file functions fails you can call the
function to find out exactly what the error was. **NOTE** : When using
the asynchronous [save](../../Buffers/buffer_save_async) /
[load](../../Buffers/buffer_load_async) functions, the [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
map will have an extra key, " **error** " which will also contain one of
the constants (shown below).

#### Syntax:

``` gml
xboxlive_get_file_error();
```

#### Returns:

``` gml
 Xbox File Error Constant
```

|                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Xbox File Error Constant](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Saving_Data/xboxlive_get_file_error)  |                                                                                                                                                                                                                                                                                                                                                        |
| Constant                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                            |
|  xboxlive_fileerror_outoflocalstorage                                                                                                   | If this occurs while saving this means that all available save game space has been used up, and the user has declined the offer (presented by the OS) of freeing up space. The game should confirm with the user that they intend to continue playing without saving. If they still want to be able to save, the game should retry the save operation. |
|  xboxlive_fileerror_quotaexceeded                                                                                                       | If this occurs the game should notify the user that they can't save any more data until they free up some space, and then present them with a way of doing this.                                                                                                                                                                                       |
|  xboxlive_fileerror_noerror                                                                                                             | The file save or load function was carried out without issues.                                                                                                                                                                                                                                                                                         |

#### Example:

``` gml
buffer_save(buff, "SaveGame.bin");
if (xboxlive_get_file_error() != xboxlive_fileerror_noerror)
{
    show_debug_message("Save failed. Error code = " + string(xboxlive_get_file_error()));
}
```

The above code checks to see if there was an error with saving and if so
the error code is printed out to the console.
