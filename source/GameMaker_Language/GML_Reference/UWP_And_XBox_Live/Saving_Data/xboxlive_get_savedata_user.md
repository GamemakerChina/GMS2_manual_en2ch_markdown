# xboxlive_get_savedata_user

This function returns the user ID pointer currently associated with file
saving (or the constant pointer_null if no user ID is currently being
used). See [ xboxlive_set_savedata_user()
](xboxlive_set_savedata_user) for further details.

#### Syntax:

``` gml
xboxlive_get_savedata_user();
```

#### Returns:

``` gml
 Xbox User ID

or

 pointer_null
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
