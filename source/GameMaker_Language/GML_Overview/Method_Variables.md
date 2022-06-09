# Method Variables

A method variable is essentially a variable that has had a function
assigned to it, "binding" the function to an instance and enabling you
to use the variable to refer to the function - much like you use a
[runtime function name](Runtime_Functions) to refer to a built-in
GML function. The variable used can be *local* , *instance* or *global*
in scope (see [here](Variables_And_Variable_Scope) for more
information on variable scope). Also see: [Script Functions vs.
Methods](Script_Functions_vs_Methods)

## Creating Methods

The syntax for creating a method variable is as follows:

``` gml
name = function( parameter1, parameter2, ... )
{
    statement1;
    statement2;
    ...
}
```

or

``` gml
function name( parameter1, parameter2, ... )
  {
    statement1;
    statement2;
    ...
}
```

To create a function in GML Visual, use [Declare A New
Function](../../Drag_And_Drop/Drag_And_Drop_Reference/Common/Declare_A_New_Function)
. Enable its "Temp" option to create a method variable (first syntax
shown above). In general, however, you would use the *first* form for
methods, and the second form for defining [script
functions](Script_Functions) , since the second form will also
assign a script index to the function name while the first form will be
a "true" method (and require the use of the
[global](Variables/Global_Variables) prefix if used to define a
scripted function). NOTE You can check this by using both forms in
project and then calling the runtime function
[typeof()](../GML_Reference/Variable_Functions/typeof) on each of
them. One will be classed as a "number" - since it returns a script
index ID - and the other will be classed as a "method". So, keep in mind
that - in general - we will always be referring to functions that have
*not* been defined with a script index when we are talking about methods
and method variables. Below you can see three simple examples of
creating a method variable using different scopes:

``` gml
// Local
var _debug = function(message)
{
    show_debug_message(message);
}

// Instance
do_maths = function(val1, val2, val3)
{
    return (val1 * val2) - val3;
}

// Global
global.pd = function(_x1, _y1, _x2, _y2);
{
    return point_distance(_x1, _y1, _x2, _y2);
}
```

Notice that in the above code, the various parameters that are given as
inputs for the function are all named and these names are what should be
used within the function to refer to the different inputs. Also note
that you can use the [return](Language_Features/return) statement to
return a value from a function for use elsewhere in your code, and
that a function with *no* return value defined, will return undefined
.by default. NOTE While the variable will be in the chosen scope, the
actual function will be bound to the scope that it was initially defined
in. For example, [script functions](Script_Functions) are all global
scope and "unbound" (ie: they are not associated with any instances),
but if you have a script function that creates another function as a
method variable within it and then you call this script function from an
instance, the function used within the script will **be bound to the
instance variable as a method** . In general this is not something you
ever need to think about but for more complex operations with method
variables it's worth taking into consideration. This also applies when
using other constructs like [ with ](Language_Features/with) - when
you create a method variable inside a with, the function will be bound
to the instance that is currently in scope. Once created, the method
variable can be used just as you would a runtime function or a script
function, for example:

``` gml
create_vec = function(_x1, _y1, _x2, _y2);
{
    var _array;
    _array[0] = point_distance(_x1, _y1, _x2, _y2);
    _array[1] = point_direction(_x1, _y1, _x2, _y2);
    return _array;
}

vec = create_vec(x, y, mouse_x, mouse_y);
```

Variables created within a function will follow the same rules as normal
and will be scoped according to the keyword used or the scope of the
function call. In the above example, we use var so the array variable is
in the *local* scope of the function. If we didn't use the keyword, then
the variable would have been created on the scope of the instance that
called the function. Methods, just like script functions, can also take
optional arguments that have default values for when they're not passed
in:

``` gml
create_attachment = function(_attachment, _x = x, _y = y)
{
    return instance_create_layer(_x, _y, layer, _attachment);
}
```

The above function takes three arguments, where the last two are
optional. If they are not passed in when the function is called, then
they'll use the instance's x and y coordinates by default. Note that if
an argument is not passed in, and it does not have a default value, then
it will be equal to undefined . Methods can also make use of static
variables, which maintain their values throughout every function call.
Please [read this page](Functions/Static_Variables) for more
information. Below we list a few helper functions associated with method
variables:

-   [is_method](../GML_Reference/Variable_Functions/is_method)
-   [method](../GML_Reference/Variable_Functions/method)
-   [method_get_self](../GML_Reference/Variable_Functions/method_get_self)
-   [method_get_index](../GML_Reference/Variable_Functions/method_get_index)
