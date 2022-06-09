# alarm_get

This function can be used to get the current value of the given alarm.
You supply the alarm number from 0 to 11 and this function will return
the value that the alarm is currently on. This is an alternative method
to getting the [alarm array](Instance_Variables/alarm) value
directly.

#### Syntax:

``` gml
alarm_get(index);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The alarm index to get, from 0 to 11. |

#### Returns:

``` gml
 Real

(integer)
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
