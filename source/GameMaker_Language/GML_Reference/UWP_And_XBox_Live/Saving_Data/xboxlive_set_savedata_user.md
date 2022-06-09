# xboxlive_set_savedata_user

This function specifies that future file operations which operate in the
save game area (i.e. all file writes, and reads from files that aren't
in the bundle area) will be associated with the specified user ID
pointer. This can be called as often as necessary to redirect save data
to the appropriate user, or you can use the constant pointer_null to
save to the generic machine storage area.

#### Syntax:

``` gml
xboxlive_set_savedata_user(user_id);
```

|          |                                                                                                                                                                                                                 |                                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                            | Description                                                  |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user) or [pointer_null](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The user ID (a pointer) to set for saving, or pointer_null   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (xboxlive_get_savedata_user() != user_id[0])
{
    xboxlive_set_savedata_user(user_id[0]);
}
```

The above code checks to see if a user is currently assigned as the save
target, and if they are not then they are assigned.
