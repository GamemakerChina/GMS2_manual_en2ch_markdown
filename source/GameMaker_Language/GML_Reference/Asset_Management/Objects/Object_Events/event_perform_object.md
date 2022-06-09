# event_perform_object

This functions works the same as [ event_perform() ](event_perform)
except that this time you can specify events from another object. There
are many options here which allow complete simulation of all possible
events, but note that this literally just performs all the code in the
event and the game will not modify anything to make it trigger itself
manually, for example if you choose to perform a keyboard press event,
the event will be triggered but the relevant key will not be recognised
as having been pressed. Or if you perform an alarm event, the alarm
counter will not be set to -1 but rather continue to count down. You can
find a complete list of the available constants this function requires
from the the page for the function [ event_perform()
](event_perform) . NOTE Actions in the event called with this
function are applied to the **current instance** , and not to instances
of the given object.

#### Syntax:

``` gml
event_perform_object(obj, type, numb);
```

|          |                                                                                                                                                                                                                      |                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                                 | Description                                                      |
| obj      |  [Object Asset](../../../../../../The_Asset_Editors/Objects)                                                                                                                                                     | The object that should have its event triggered.                 |
| type     |  [Event Type Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Objects/Object_Events/event_perform)                                                                                  | The type of event to perform.                                    |
| numb     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Event Number Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Objects/Object_Events/event_perform)    | The specific event, if one is necessary (otherwise, just use 0). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
event_perform_object(obj_Player, ev_keypress, ord("W"));
```

This would perform the event associated with Keyboard Check Pressed \> W
key from the object "obj_Player" in the current instance.
