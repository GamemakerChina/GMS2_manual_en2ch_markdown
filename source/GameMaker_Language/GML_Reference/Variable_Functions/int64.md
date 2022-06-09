# int64

This function will attempt to convert a given value into a 64bit
integer, where the value *must* be either a real, a string, an int64 ,
an int32 , or a ptr . Anything else will cause the game to crash with an
error message. You can check to see if a variable holds an int64 using
the function [ is_int64() ](is_int64) .

#### Syntax:

``` gml
int64(val);
```

|          |                                                                                                                                                                                                                            |                       |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                                                                                                                                                                       | Description           |
| val      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types) , [String](../../../../GameMaker_Language/GML_Overview/Data_Types) , or [Pointer](../../../../GameMaker_Language/GML_Overview/Data_Types)      | The value to convert. |

#### Returns:

``` gml
 int64 (64-bit integer)
```

#### Example:

``` gml
steam_handle = int64(global.fileReadString);
```

The above code converts the value held in the global variable to a 64bit
integer.
