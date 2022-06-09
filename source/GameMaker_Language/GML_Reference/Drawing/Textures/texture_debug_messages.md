# texture_debug_messages

This function can be used to enable or disable texture debug messages.
When enabled (set to true ), additional information about texture page
use will be sent to the output window. Set to false to disable this
output again.

#### Syntax:

``` gml
texture_debug_messages(enable);
```

|          |                                                                            |                                              |
|----------|----------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                       | Description                                  |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable or disable the texture debug messages |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if global.debug
{
    texture_debug_messages(true);
}
```

The above code will check the value of a global variable and if it is
set to true then texture debug messages are enabled.
