# os_check_permission

With this function you can check to see if a specific permission has
been granted to the game by the user. You supply the permission to check
as a string using the format " android.permission. ", so to check the
RECORD_AUDIO permission (for example) you would call

``` gml
os_check_permission("android.permission.RECORD_AUDIO");
```

The function will return will return one of three constants - shown
below - to tell the game how the state of the permission. For more
information on app permissions, please see the [Android
Documentation](https://developer.android.com/guide/topics/permissions/overview)
. **IMPORTANT!** This function is for the **Android** target only.

#### Syntax:

``` gml
os_check_permission(permission)
```

|            |                                                                        |                                    |
|------------|------------------------------------------------------------------------|------------------------------------|
| Argument   | Type                                                                   | Description                        |
| permission |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The permission to check (a string) |

#### Returns:

``` gml
 Permission State Constant
```

|                                                                                                                     |                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  [Permission State Constant](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/os_check_permission)  |                                                                                                                                                                      |
| Constant                                                                                                            | Description                                                                                                                                                          |
|  os_permission_granted                                                                                              | This indicates that the permission has been granted                                                                                                                  |
|  os_permission_denied                                                                                               | This indicates that the permission has not been granted                                                                                                              |
|  os_permission_denied_dont_request                                                                                  | This indicates that the permission has either been blocked by the phone settings, or that the user has previously denied the request and selected "Don't ask again". |

#### Example:

``` gml
if (os_type == os_android)
{
    if (os_check_permission("android.permission.INTERNET") == os_permission_denied)
    {
        os_request_permission("android.permission.INTERNET");
    }
}
```

The above code checks the OS type and if is Android, it performs a check
on the permissions and if the "INTERNET" permission has not yet been
granted, it requests it.
