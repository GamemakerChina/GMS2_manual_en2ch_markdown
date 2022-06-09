# xboxlive_pad_count_for_user

With this function you can find out how many pad "slots" are active for
the current user (see [ xboxlive_pad_for_user()
](xboxlive_pad_for_user) for further details).

#### Syntax:

``` gml
xboxlive_pad_count_for_user(user_id, slot);
```

|          |                                                                                                                              |                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                                         | Description                      |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) to check |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
global.slots[0] = xboxlive_pad_count_for_user(user_id[0])
```

The above code stores the number of pads associated with the given user
ID pointer.
