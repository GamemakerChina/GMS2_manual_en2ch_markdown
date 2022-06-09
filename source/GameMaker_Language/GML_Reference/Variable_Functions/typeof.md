# typeof

This function returns the data type of any given variable as a string.
The possible return values are listed in the table below:

|           |                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| String    | Description                                                                                                                               |
| number    | The variable holds a real (floating point) number - this can include NaN and infinity                                                     |
| string    | The variable holds a string                                                                                                               |
| array     | The variable references an array                                                                                                          |
| bool      | The variable holds a boolean ( true / false )                                                                                             |
| int32     | The variable holds a 32bit integer                                                                                                        |
| int64     | The variable holds a 64 bit integer                                                                                                       |
| ptr       | The variable holds a pointer                                                                                                              |
| undefined | The variable is undefined                                                                                                                 |
| null      | The variable holds a null value (this should not be seen normally)                                                                        |
| vec3      | The variable holds a 3 value vector                                                                                                       |
| vec4      | The variable holds a 4 value vector                                                                                                       |
| method    | The variable holds a function reference                                                                                                   |
| struct    | The variable holds a struct reference                                                                                                     |
| unknown   | Value is unknown. This should *never* be seen and signifies that something has gone wrong at the most basic level like a memory overwrite |

Please note that there are cases when this function may not return the
correct value for a **method** . Consider the following two function
definitions:

``` gml
a = function()
{
    // something
}

function b()
{
    // Something
}
```

Technically, these are both considered methods as they are binding a
function to an instance scope variable, however calling typeof() on
function b will return "number" and *not* "method", while calling it on
a will return "method". This is due to the fact that methods created
like the one for b are assigned script indices (which are integer
values), since this is the way that the compiler recognises
script functions, even if the function was not defined in a script.

#### Syntax:

``` gml
typeof(variable);
```

|          |                                                                                   |                                       |
|----------|-----------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                              | Description                           |
| variable |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The variable to get the data type of. |

#### Returns:

``` gml
 String

(see table above)
```

#### **Example:**

``` gml
var _str = typeof(global.ExtensionInput);
show_debug_message(" global.ExtensionInput is a " + _str);
```

The above code gets the data type held by the given global variable and
returns the string to a local variable which is then used to output a
message to the console.
