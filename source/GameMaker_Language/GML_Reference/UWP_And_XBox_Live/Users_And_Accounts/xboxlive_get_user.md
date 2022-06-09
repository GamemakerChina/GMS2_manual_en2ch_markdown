# xboxlive_get_user

With this function you can retrieve the user ID pointer for the indexed
user. If the user does not exist, the function will return the constant
pointer_null instead. You can find the number of users currently logged
in with the function [ xboxlive_get_user_count()
](xboxlive_get_user_count) . **IMPORTANT** : This function should
only be used with xboxlive_get_user_count()  - do not use this with
gamepads. Use [ xboxlive_user_for_pad() ](xboxlive_user_for_pad)
instead.

#### Syntax:

``` gml
xboxlive_get_user(index);
```

|          |                                                                         |                                                 |
|----------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                    | Description                                     |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index (an integer) to get the User ID from. |

#### Returns:

``` gml
 Xbox User ID

or

 pointer_null
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); ++i;)
{
    user_id[i] = xboxlive_get_user(i);
}
```

The above loops through all the signed in users and stores their unique
ID pointer in an array.
