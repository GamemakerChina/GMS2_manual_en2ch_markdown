# xboxlive_user_for_pad

This function will return the User ID pointer associated with the given
gamepad index value, or pointer_null if no user is associated with it.
Note that this function should only be used with gamepad indices, and
**not** with [ xboxlive_get_user_count() ](xboxlive_get_user_count)
.

#### Syntax:

``` gml
xboxlive_user_for_pad(pad_index);
```

|           |                                                                         |                                                     |
|-----------|-------------------------------------------------------------------------|-----------------------------------------------------|
| Argument  | Type                                                                    | Description                                         |
| pad_index |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index (an integer) of the gamepad slot to check |

#### Returns:

``` gml
 Xbox User ID

or

 pointer_null
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; 11; ++i;)
{
    var u_id = xboxlive_user_for_pad(i);
    if u_id != pointer_null
    {
        pad_name[i] = xboxlive_gamedisplayname_for_user(u_id);
    }
    else
    {
        pad_name[i] = "Press Play";
    }
}
```

The above code loops through all available pad slots and checks to see
if there is a user ID pointer associated with it. If there is, an array
is set with the user display name, otherwise the array is set to some
default text.
