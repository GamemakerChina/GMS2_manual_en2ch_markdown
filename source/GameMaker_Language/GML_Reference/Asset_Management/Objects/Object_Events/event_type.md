# event_type

This **read-only** variable returns the type of event currently being
executed, which can be one of the following constants:

-   **ev_create**
-   **ev_destroy**
-   **ev_step**
-   **ev_alarm**
-   **ev_keyboard**
-   **ev_keypress**
-   **ev_keyrelease**
-   **ev_mouse**
-   **ev_collision**
-   **ev_other**
-   **ev_gesture**
-   **ev_draw**

For a full list of the constants that are related to the different
events see [ event_perform() ](event_perform) , and if you should
need the event number (ie: the sub event), you should be checking the [
event_number ](event_number) .

#### Syntax:

``` gml
event_type;
```

#### Returns:

``` gml
 Event Type Constant
```

#### Example:

``` gml
show_debug_message("Current Event = " + string(event_type));
```

The above code will show a debug message with the event type currently
being performed.
