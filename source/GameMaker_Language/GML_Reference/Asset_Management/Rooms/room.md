# room

This variable holds the room index for the current room that your game
is running. This is *not* a read only variable, however changing this
will not change the index value for the current room, but rather change
the room to match the index that you have set the variable to. Care
should be taken when doing this as if the index you change the variable
to is not valid the game will throw an error and close. In general it is
much better practice to use [ room_goto() ](room_goto) to change
rooms. **Note** : Room IDs are not based on their order in the Asset
Browser or the Room Manager, and so you should avoid supplying a number
value directly. Instead, use the room constant for the asset you want to
reference (which is simply its name) or retrieve it through a function.

#### Syntax:

``` gml
room;
```

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
if (room == rm_level1)
{
    audio_play_sound(snd_level1, 1, 1);
}
```

The above code will check if the current room is the first level, and in
that case play that level's music.
