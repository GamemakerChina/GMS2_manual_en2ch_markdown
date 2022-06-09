# event_number

This **read-only** variable returns the number of the event currently
being called, where the number is actually referring to the "sub event"
of the event, ie: for the step event the event number could be any one
of the constants **ev_step_normal** , **ev_step_begin** , or
**ev_step_end** . For a full list of constants that are available for
the specific sub-events see [ event_perform() ](event_perform) , and
if you should need to know the main event itself, you should be checking
the [ event_type ](event_type) .

#### Syntax:

``` gml
event_number;
```

#### Returns:

``` gml
 Event Number Constant
```

#### Example:

``` gml
switch (event_number)
{
    case ev_step_normal: show_debug_message("Step event!"); break;
    case ev_game_start: show_debug_message("Game Start""); break;
    case ev_room_start: show_debug_message("Room Start!"); break;
}
```

The above code could be called form a script and used to show debug
messages informing you which event is being currently triggered.
