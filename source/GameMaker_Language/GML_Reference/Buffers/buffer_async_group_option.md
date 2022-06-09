# buffer_async_group_option

With this function you can set some platform specific options for the
buffer group being saved/loaded. The options available are as follows:

-   " **subtitle** " or " **slottitle** " - The value for this option
    would be a string, which will be shown to the user when managing
    their save data in the OS. This is only important when saving data,
    not when loading again.
-   " **showdialog** " - The value for this option is a boolean true or
    false . If set to true , when you save *or* load GameMaker will show
    the System UI, otherwise it will do a quicksave/quickload with no UI
    shown. You normally only need this if you're supporting multiple
    save slots to allow the user to pick a slot, but if you just support
    one slot per user, set this to false .
-   " **savepadindex** " - For this option you would specify the *pad
    index* of the player who is saving *or* loading and the system will
    write data to and read data from this player's save folder.
-   " **saveslotsize** " - This option requires that you specify the
    actual size in bytes you want to save (so you can do a [
    buffer_seek() ](buffer_seek) and [ buffer_tell()
    ](buffer_tell) to get that, for example). Note that it is not
    obligatory to supply this value as all saves are pre-assigned a
    minimum space, which usually varies with the target platform.
-   " **ps_create_backup** " - *(PlayStation only)* - Setting this to
    true makes sure that the save data is backed up when the save
    directory is unmounted (i.e. when the
    [buffer_async_group_end()](buffer_async_group_end) function is
    called). See the console documentation for more information.

**IMPORTANT!** This function is currently only valid for the PSVita, PS4
and XBox One target modules. On all the other targets it will do
nothing.

#### Syntax:

``` gml
buffer_async_group_option(option, value);
```

|          |                                                                                                                                                |                                                                      |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Argument | Type                                                                                                                                           | Description                                                          |
| option   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The option to set.                                                   |
| value    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types) or [String](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The value to set (can be a real or string, depending on the option). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_async_group_begin("save_folder_name");
buffer_async_group_option("showdialog", false);
buffer_async_group_option("slottitle", "Catch The Haggis Save");
buffer_async_group_option("subtitle", "All your haggis are saved here!");
save = buffer_save_async(buff, "Player_Save.sav", 0, 16384);
buffer_async_group_end();
```

The above code starts a buffer group then sets the group options before
it sets 4 files to save asynchronously. The group definition is then
ended (at which point saving will begin).
