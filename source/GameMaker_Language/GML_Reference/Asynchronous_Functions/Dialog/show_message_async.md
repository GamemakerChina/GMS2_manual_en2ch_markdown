# show_message_async

This function opens a window and displays the message you define in the
function to the user. This is an asynchronous function, and as such
GameMaker does *not* block the device it is being run on while waiting
for an answer, but rather keeps on running events as normal. Once the
user has pressed the "Okay" button, an asynchronous
[**Dialog**](../../../../The_Asset_Editors/Object_Properties/Async_Events/Dialog)
event is triggered which, for the duration of that event *only* , will
have a ds_map stored in the variable [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
. This map will contain the two keys, "id" and "status", with "id" being
the value that was returned by the function when called, and the
"status" being either true for the "Okay" button being pressed, or false
if the message was cancelled (where available as not all target
platforms permit the cancellation of dialogues). *** NOTE *** *This
function is for **debugging and testing use only** and should not be
used in released games. For that purpose you should create a custom user
interface to receive input from players so that you have complete
control over how the dialogs look and behave. *

#### Syntax:

``` gml
show_message_async(string);
```

|          |                                                                           |                                  |
|----------|---------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                      | Description                      |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The message to show to the user. |

#### Returns:

``` gml
 Async Request ID
```

#### Extended Example:

The **left mouse press event** (for example) of the object that is
showing the message would have the following code:

``` gml
msg = show_message_async("You will now be taken to the store");
```

The above will show a message with the given string. The message id is
stored in the variable "msg" and will be used in the asynchronous
Dialogs event as shown below:

``` gml
var i_d, stat;
i_d = ds_map_find_value(async_load, "id");
if i_d == msg
{
    if ds_map_find_value(async_load, "status")
    {
        url_open("https://play.google.com/store");
    }
}
```

The above code checks the "id" key of the returned DS Map against the
value stored in the variable "msg". If they are the same, it then checks
to see if the "Okay" button was pressed (rather than the window being
closed/cancelled) and if it returns true it opens a url.
