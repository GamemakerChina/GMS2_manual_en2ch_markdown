# external_call

If you have created an external function call to a dll or dylib using [
external_define() ](external_define) , you can use this function to
then call it. You supply the name of the previously defined function as
well as each of the arguments it requires (each argument must be of the
correct type, either real or string) and the function returns the result
of the external call.

#### Syntax:

``` gml
external_call(id, args[0...15]);
```

|                |                                                                                                                                                |                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Argument       | Type                                                                                                                                           | Description                                                                    |
| id             |  [External Function](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/external_define)                                         | The name of the function that you want to call                                 |
| args\[0...10\] |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types) or [String](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The different arguments that you want to pass through to the external function |

#### Returns:

``` gml
 Variable

(the type of value returned will depend on the defined function)
```

#### Example:

``` gml
my_function = external_define("MyDLL.dll", "MyMin", dll_cdecl, ty_real, 2, ty_real, ty_real);
var _a = external_call(my_function, x, y);
```

The above example code calls a previously defined external function and
stores the returned value in a local variable.
