# ln

The natural logarithm ln(n) is the amount of time needed to reach a
certain level of continuous growth, where n is the level reached. So if
we want to find out how many time units we need to get 20 growth we
would use ln(20) which returns 2.99 units of time to get that amount of
growth.

#### Syntax:

``` gml
ln(n);
```

|          |                                                                         |                  |
|----------|-------------------------------------------------------------------------|------------------|
| Argument | Type                                                                    | Description      |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The input value. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
alarm[0] = ln(age) * room_speed;
```

The above code uses the natural logarithm of the value stored in the
variable "age" to set an alarm.
