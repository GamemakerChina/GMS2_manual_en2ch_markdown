# highscore_add

With this function you can add a name and a score to the internal global
high score list. There is no need to check the value to see if it is
high enough to enter into the score list as GameMaker will only store
those values that are greater than the tenth position stored.

#### Syntax:

``` gml
highscore_add(str, numb);
```

|          |                                                                        |                                              |
|----------|------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                   | Description                                  |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string (name) to attribute the score to. |
| numb     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The number (score) to add.                   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (lives == 0)
{
    highscore_add(global.Name, score);
    score = 0;
    room_goto(rm_MainMenu);
}
```

The above code will check the lives and if they are set to 0, it will
add the current score and the string held in the global variable "Name"
into the high score list, before finally setting the score to 0 and
sending the player to the room indexed in "rm_MainMenu".
