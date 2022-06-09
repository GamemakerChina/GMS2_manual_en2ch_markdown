# external_define

This function can be used to define an external function call to a
specific dll (for Windows) or dylib (for Mac). This file can be either
an included file or part of an extension. You supply the name (and path)
of the file, then the name of the function that you wish to define. Next
you need to define the calling convention to be used (see the constants
list below) as well as the type of result to be expected (also a
constant, as listed below). Finally you must give the number of
arguments that the function can take (from 0 to 15) and for each of the
arguments you must specify its type too. Please note that for functions
with 4 or more arguments, all of them *must* be of type ty_real .
**NOTE** : This is only for dll or dylib that have been added as
"Included Files" to the GameMaker IDE. It will not work with those files
added as extensions, since those require that you define the functions
in the extension package itself.

|                              |                                                       |
|------------------------------|-------------------------------------------------------|
| External Call Type Constants |                                                       |
| Constant                     | Description                                           |
|  dll_cdecl                   | This is the default C, C++ call                       |
|  dll_stdcall                 | This is the standard WinAPI call (Windows dll only)   |

|                              |                                   |
|------------------------------|-----------------------------------|
| External Data Type Constants |                                   |
| Constant                     | Description                       |
|  ty_real                     | A real number argument            |
|  ty_string                   | A null-terminated string argument |

#### Syntax:

``` gml
external_define(dll, name, calltype, restype, argnumb, argtype[0], argtype[1], ...argtype[10]);
```

|                     |                                                                                                                             |                                       |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument            | Type                                                                                                                        | Description                           |
| dll                 |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The name of the DLL file (string)     |
| name                |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The name of the function (string)     |
| calltype            |  [External Call Type Constant (dll\_\*)](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/external_define)  | The calling convention used           |
| restype             |  [External Data Type Constant (ty\_\*)](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/external_define)   | The type of the result to expect      |
| argnumb             |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                         | The number of arguments (0 - 10)      |
| argtype\[0 ... 10\] |  [External Data Type Constant (ty\_\*)](../../../../GameMaker_Language/GML_Reference/OS_And_Compiler/external_define)   | The types of the arguments being used |

#### Returns:

``` gml
 External Function
```

#### Example:

``` gml
my_funcion = external_define("MyDLL.dll", "MyMin", dll_cdecl, ty_real, 2, ty_real, ty_real);
```

The above example code will define an external function called "MyMin"
with two arguments.
