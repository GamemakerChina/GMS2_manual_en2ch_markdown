# alarm_set

This function can be used to set an alarm. You supply the alarm number
from 0 to 11, and then the value to set the alarm to. The value must be
an integer value, and you can set it to -1 to stop the alarm (non
integer values will be rounded to the nearest integer). This is an
alternative method to setting the [alarm
array](Instance_Variables/alarm) directly.

#### Syntax:

``` gml
alarm_set(index, value);
```

|          |                                                                         |                                             |
|----------|-------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                    | Description                                 |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The alarm index to set, from 0 to 11.       |
| value    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value (an integer) to set the alarm to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; 12; i++)
{
    if alarm_get(i) &amp;gt; 0 alarm_set(i, -1);
}
```

The above code checks all the alarms in the calling instance and if they
are greater than 0 it sets them to -1, stopping them from counting down
any further.
