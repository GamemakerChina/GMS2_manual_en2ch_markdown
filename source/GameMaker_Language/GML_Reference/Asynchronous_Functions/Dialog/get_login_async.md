# get_login_async

This function opens a window that asks the user to input a username and
password. These arguments can be set as an empty string or you can store
previously entered values to use if you wish. This is an asynchronous
function, and as such GameMaker does *not* block the device it is being
run on while waiting for an answer, but rather keeps on running events
as normal. Once the user has input the details and pressed the "Okay"
button, an asynchronous **User Interaction** event is triggered which,
for the duration of that event *only* , will have a DS map stored in the
variable [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
. This map will contain the two keys, " **username** " and "
**password** ", with the corresponding user input stored in each. As it
is a DS Map that has been created, this can then be used, for example,
by the [ json_encode()
](../../File_Handling/Encoding_And_Hashing/json_encode) function
ready to be sent to a server or written to a file on the chosen device.
This function will return an index number for the async event that was
triggered, which can then be checked in the corresponding event so that
you can "target" specific data in case you're expecting more than one
async events to be triggered (perhaps from some other function). ***
NOTE *** *This function is for **debugging and testing use only** and
should not be used in released games. For that purpose you should create
a custom user interface to receive input from players so that you have
complete control over how the dialogs look and behave. *

#### Syntax:

``` gml
get_login_async(name, password);
```

|          |                                                                           |                       |
|----------|---------------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                      | Description           |
| username |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The default user name |
| password |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The default password  |

#### Returns:

``` gml
 Async Request ID
```

#### Extended Example:

The **create event** (for example) of the object that is controlling the
login of our user would have the following code:

``` gml
ini_open("Profile.ini");
u = ini_read_string("User","0","");
p = ini_read_string("User","1","");
ini_close();
login = get_login_async(u,p);
```

The above code opens an ini file (or creates one if it doesn't exist)
and gets the name and password stored in that file. If they do not
exist, then the default of an empty string ("") is returned. These
values are then used in get_login_async() to ask the user for their
username and password details, with the request index being stored in
the variable "login". Note that while waiting for the user to give the
necessary information the game and its events will continue to run as
normal. Now that the asynchronous code has been fired off, we need to
check for the return value in the [asynchronous event for
Dialogs](../../../../The_Asset_Editors/Object_Properties/Async_Events/Dialog)
in the following way:

``` gml
if ds_map_find_value(async_load, "id") == login
{
    u = ds_map_find_value(async_load, "username");
    p = ds_map_find_value(async_load, "password");
}
```

The above code checks the "id" key of the async_load DS map and if it
holds the same value as that stored in the "login" variable, the map
details are then read into the corresponding variables which you can
then store or use to check against database values etc...
