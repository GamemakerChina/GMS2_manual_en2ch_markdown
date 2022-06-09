# clamp

With this function you can maintain an input value between a specified
range.

#### Syntax:

``` gml
clamp(val, min, max)
```

|          |                                                                         |                                     |
|----------|-------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                    | Description                         |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The value to clamp.                 |
| min      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The minimum value to clamp between. |
| max      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum value to clamp between. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
speed = clamp(speed, 1, 10);
```

The above code will clamp the speed so that it never falls below 1 or
goes over 10.
