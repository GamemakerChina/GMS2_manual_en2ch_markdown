# show_message

This function creates a pop-up message box which displays the given
string and a button marked "Ok" to close it. ** NOTE ** This function is
for **debug use only** on Desktop targets and UWP, but is **deprecated**
on all other targets.

#### Syntax:

``` gml
show_message(str);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to show in the pop-up message. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var tot = 0;
for (var i = 0; i &amp;lt; 10; i += 1)
{
    tot += inv[i];
}
show_message("Total = " + string(tot));
```

The above code will loop through the values stored in the array "inv"
and add them to the variable "tot" before showing a message with the
total.
