# get_string_async

This function opens a window and displays message as well as a space for
the user to input a string (which will contain the supplied default
string to start with). This is an asynchronous function, and as such
GameMaker does *not* block the device it is being run on while waiting
for an answer, but rather keeps on running events as normal. Once the
user has typed out their string and pressed the "Okay" button, an
[asynchronous Dialog
event](../../../../The_Asset_Editors/Object_Properties/Async_Events/Dialog)
is triggered which, for the duration of that event *only* , will have a
DS map stored in the variable [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
. This map will contain the three keys, " **id** ", " **status** ", and
" **result** ". "id" is the value that was returned by the function when
called, the "status" will be either true for the "Okay" button being
pressed, or false if the message was cancelled (where applicable as not
all target platforms permit the message to be cancelled). Finally
"result" will return the string that the user input (or an empty string
"" if none was supplied). *** NOTE *** *This function is for **debugging
and testing use only** and should not be used in released games. For
that purpose you should create a custom user interface to receive input
from players so that you have complete control over how the dialogs look
and behave. *

#### Syntax:

``` gml
get_string_async(string, default);
```

|          |                                                                           |                                    |
|----------|---------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                      | Description                        |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The message to show in the dialog. |
| default  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The default string.                |

#### Returns:

``` gml
 Async Request ID
```

#### Extended Example:

The **left mouse press event** (for example) of the object that is
showing the message would have the following code:

``` gml
msg = get_string_async("What's your name?","Anon");
```

The above will show a message requesting that the user input a string
and press "Okay". The function id is stored in the variable "msg" and
will be used in the asynchronous Dialogs event as shown below:

``` gml
var i_d = ds_map_find_value(async_load, "id");
if i_d == msg
{
    if ds_map_find_value(async_load, "status")
    {
        if ds_map_find_value(async_load, "result") != ""
        {
            global.Name = ds_map_find_value(async_load, "result");
        }
    }
}
```

The above code checks the "id" key of the returned DS Map against the
value stored in the variable "msg". If they are the same, it then checks
to see if "Okay" was pressed (rather than the window being
closed/cancelled) and if it returns true it then checks the "result" of
a string to make sure that no empty strings were returned before setting
a global variable.
