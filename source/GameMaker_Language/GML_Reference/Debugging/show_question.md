# show_question

This function creates a pop-up message box with two buttons for "Yes"
and "No". It returns true or false depending on which one of the two
buttons the user presses. ** NOTE ** This function is for **debug use
only** on Desktop targets, but is **deprecated** on all other targets.

#### Syntax:

``` gml
show_question(str);
```

|          |                                                                        |                                            |
|----------|------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                   | Description                                |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to show in the pop-up question. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (score &amp;gt; 500) &amp;amp;&amp;amp; debug_mode
{
    if show_question("Continue to next room?")
    {
        room_goto(rm_Level2);
    }
    else game_end();
}
```

The above code will check the score and if it is over 500, it will ask
the user if they wish to continue or not and if the "yes" button is
clicked it will go to another room, but if the "no" button is selected
it will end the game.
