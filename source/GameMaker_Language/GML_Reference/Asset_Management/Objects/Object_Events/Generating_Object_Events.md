# Generating Object Events

GameMaker is completely event driven, and that all actions happen as the
result of certain events that are triggered in a specific order or by a
specific occurrence within the game. There are a number of different
events, each one with a specific task or timing and some of them are
even split into separate "sub" events. Normally these events are run by
GameMaker when it detects an in-game trigger, or every game tick (as is
the case with the step and draw events), but you can also apply an event
to an instance in the current room from within a piece of code. The
following functions exist that deal with generating events:

-   [event_inherited](event_inherited)
-   [event_perform](event_perform)
-   [event_perform_async](event_perform_async)
-   [event_perform_object](event_perform_object)
-   [event_user](event_user)

There are also a number of read only variables that can be used with the
functions listed above which are particularly useful for debugging:

-   [event_action](event_action)
-   [event_number](event_number)
-   [event_object](event_object)
-   [event_type](event_type)

For more information on events please see the section [Object
Events](../../../../../The_Asset_Editors/Object_Properties/Object_Events)
.
