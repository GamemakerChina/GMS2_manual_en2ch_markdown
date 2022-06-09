# shop_leave_rating

This function opens up an OS dependent dialog where you can ask the user
to post a rating or comment to a particular page. You can define the
text that is to appear in the dialogue, as well as the text you wish to
appear on the two buttons and the URL where the comment has to be
posted. **NOTE** : This function is only for Android and iOS targets.
**IMPORTANT!** On **iOS** , when using TestFlight, in development the
prompt will be displayed but you won't be able to actually do anything.
Once your app is in the App Store, this button becomes active and the
user is given the option to write a review or leave a rating. Note that
if you distribute the game through TestFlight, this window may not even
be shown.

#### **Syntax:**

``` gml
shop_leave_rating(text, yes_string, no_string, url)
```

|            |                                                                           |                                                |
|------------|---------------------------------------------------------------------------|------------------------------------------------|
| Argument   | Type                                                                      | Description                                    |
| text       |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Text that appears on the dialog.               |
| yes_string |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Text that appears on the "yes" button.         |
| no_string  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Text that appears on the "no" button.          |
| url        |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The full URL where the comment has to be sent. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if timer &amp;lt;= 0
{
    shop_leave_rating("Thanks for playing the game! Why not leave a comment?", "Okay!", "Not Today!", "http://MacSweeney/comments");
    timer = 10000000;
}
else
{
    timer -= 1;
}
```

The above code will ask the user to leave a comment if the variable
"timer" has counted down to 0.
