# os_check_permission

With this function you can request a specific permission. You supply the
permission to request as a string using the format " android.permission.
", so to request the RECORD_AUDIO permission (for example) you would
call

``` gml
os_request_permission("android.permission.RECORD_AUDIO");
```

The function will return trigger a [System Asynchronous
Event](../../../The_Asset_Editors/Object_Properties/Async_Events/System)
where the built in [ async_load
](../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map will contain the following key/value pairs:

-   " **type** ": This is the event type that was triggered and the
    value will be the string " permission_request_result ".
-   " ": This will the permission requested by the function as a string,
    which will contain one of the following constants:

|                         |                                                         |
|-------------------------|---------------------------------------------------------|
| Constant                | Description                                             |
|  os_permission_granted  | This indicates that the permission has been granted     |
|  os_permission_denied   | This indicates that the permission has not been granted |

It is worth noting that the following permission are supported natively
by GameMaker , but are considered "dangerous" by Google and as such they
*must* be explicitly requested (note too that some permissions can be
requested using the [Android Game
Options](../../../Settings/Game_Options/Android) without the need
for this function):

-    android.permission.WRITE_EXTERNAL_STORAGE
-    android.permission.READ_PHONE_STATE
-    android.permission.RECORD_AUDIO

For more information on app permissions, please see the [Android
Documentation](https://developer.android.com/guide/topics/permissions/overview)
. **IMPORTANT!** This function is for the **Android** target only.

#### Syntax:

``` gml
os_request_permission(permission)
```

|            |                                                                        |                                      |
|------------|------------------------------------------------------------------------|--------------------------------------|
| Argument   | Type                                                                   | Description                          |
| permission |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The permission to request (a string) |

#### Returns:

``` gml
N/A
```

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
