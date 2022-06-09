# event_data

This variable is **global** in scope and is used to hold a [DS
Map](../../Data_Structures/DS_Maps/DS_Maps) when used in the
appropriate event (e.g. [Gesture
Events](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
and [Broadcast
Messages](../../../../The_Asset_Editors/Sequence_Properties/Broadcast_Messages)
), and -1 at all other times. The actual contents of the DS map will
depend on the type of event that triggered it, so refer to the
individual sections for those events.

#### Syntax:

``` gml
event_data;
```

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
isFlick = event_data[?"isflick"];

if (isFlick)
{
    flickVelX = event_data[?"diffX"];
    flickVelY = event_data[?"diffY"];
}
else
{
    flickVelX = 0;
    flickVelY = 0;
}
```

The above code is taken from the **Drag End** gesture event and checks
to see if the vent is a "flick" event, and if it is it extracts the
required data from the event_data DS map and uses it to set some
variables. If a "flick" event is not detected, then the same variables
are set to 0.
