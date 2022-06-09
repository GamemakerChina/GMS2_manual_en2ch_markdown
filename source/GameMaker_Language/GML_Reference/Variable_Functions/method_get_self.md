# method_get_self

With this function you can retrieve the instance ID or struct reference
which is the [ self ](../../GML_Overview/Instance_Keywords) context
used when the method is called. If the variable is *not* a method then
the function will return undefined . Please note that the function may
also return the constant pointer_null , in which case the current self
is being used at the time of the call.

#### Syntax:

``` gml
method_get_self(method);
```

|          |                                                                              |                               |
|----------|------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                         | Description                   |
| method   |  [Method](../../../../GameMaker_Language/GML_Overview/Method_Variables)  | The method variable to check. |

#### Returns:

``` gml
 Instance ID

,

 Struct

,

 undefined

, or

 pointer_null
```

#### Example:

``` gml
var _self = method_get_self(light_properties);
show_debug_message(string(_self));
```

The above code gets the self context for the given method variable and
outputs it to the console.
