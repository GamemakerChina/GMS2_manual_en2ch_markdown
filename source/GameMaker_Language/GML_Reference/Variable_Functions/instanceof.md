# instanceof

This function can be used to get the name of the [constructor
function](../../GML_Overview/Structs) that was used to create a
struct. The struct itself should have been created using the [
](../../GML_Overview/Language_Features/new) [ new
](../../GML_Overview/Language_Features/new) operator along with the
constructor itself. You supply the variable with the struct reference to
check and the function will return either a string with the constructor
name or undefined . Note that if you pass the function a struct literal
(i.e.: a struct that was created without using a constructor function)
then it will simply return the string "struct" . This function can also
be used to check if a struct reference is a **weak reference** or not,
in which case the function will return the string "weakref" instead of
the name of the function that created the struct. For more information,
see the function [ weak_ref_create()
](../Garbage_Collection/weak_ref_create) . The returned constructor
name will include additional text if the constructor function was not
created in a script. If it was created inside an object, its name will
include the object and the event where it was created. For example, a
constructor called test_constructor created in the Create event of
**Object1** will be returned as
"test_constructor_gml_Object_Object1_Create_0" . To avoid this, create
your constructors in a [script](../../GML_Overview/Script_Functions)
.

#### Syntax:

``` gml
instanceof(struct_id);
```

|          |                                                                     |                              |
|----------|---------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                | Description                  |
| struct   |  [Struct](../../../../GameMaker_Language/GML_Overview/Structs)  | The struct reference to use. |

#### Returns:

``` gml
 String

or

 undefined
```

#### Extended Example:

In this example we must first define the function that will be used as
the constructor for our struct. The following function is defined in a
script asset:

``` gml
function init_struct(_a, _b, _c) constructor
{
    a = _a;
    b = _b;
    c = _c;
}
```

This function can then be used along with the new operator to create a
struct and populate it with the variables set to the values of the
arguments used in the function:

``` gml
mystruct = new init_struct(10, 100, "Hello World");
```

We can then get the name of the constructor function that was used like
this:

``` gml
var _name = instanceof(mystruct);
if is_string(_name)
{
    show_debug_message(_name);
}
```

This will print the string "init_struct" to the output log, which is the
name of the constructor function as defined in its script.
