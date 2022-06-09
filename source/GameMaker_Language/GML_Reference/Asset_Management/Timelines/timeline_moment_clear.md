# timeline_moment_clear

With this function you can clear a specific moment of any previously
defined time line of all codes and actions.

#### Syntax:

``` gml
timeline_moment_clear(ind, step);
```

|          |                                                                         |                                     |
|----------|-------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                    | Description                         |
| ind      |  [Timeline Asset](../../../../../The_Asset_Editors/Timelines)       | The index of the timeline to clear. |
| step     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The moment to clear.                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
timeline_moment_clear(global.tl, room_speed * 30);
```

The above code will clear the specified moment of the time line indexed
by the variable "global.tl".
