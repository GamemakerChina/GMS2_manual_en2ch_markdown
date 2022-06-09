# event_user

With this function you tell the instance to run the actions or code that
has been placed within one of the 16 user defined events. These events
can *only* be called in this way, or using the [ event_perform
](event_perform) function.

#### Syntax:

``` gml
event_user(numb);
```

|          |                                                                            |                                                     |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                       | Description                                         |
| numb     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of User Event to call, between 0 and 15. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
event_user(4);
```

This would call User Defined Event 4.
