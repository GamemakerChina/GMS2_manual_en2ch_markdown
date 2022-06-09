# Variables And Variable Scope

Like any programming language **GML** uses *variables* as the basic unit
for most programming operations. Variables are used to store information
in the devices memory for later (or instant) use, and they are given a
name so that you can refer to them in runtime and script functions. A
variable in **GML** can store many different [**data
types**](Data_Types) , like a real number (eg: 100, 2.456575, -56
etc...), a string (eg: "Hello world!"), an integer (eg: 1, 556, -7), or
a boolean ( true or false ), as well as other things:

``` gml
var _num = 126.4545;
var _str = "Hello World";
new_num = _num * 100;
global.my_string = _str + " I said";
```

You can also use variables to hold the values returned from functions,
for example:

``` gml
var _id = instance_nearest(x, y, obj_Tree);
root = sqrt(1000);
global.str = string_upper("Hello World");
```

So, a variable is something that we can name and use to store a value
for later use in one or more operations. A great "real world" example of
a variable is **pi 𝜋** ... it is a variable that everyone knows and it
holds the value 3.14159265(etc...). Why do we have it in our language?
Well, it's much easier to say to someone "pi" than "three point one four
one five nine two six five"! Naming things like this makes life a lot
simpler and it also means that should the value of that variable ever
change, we don't have to change the number everywhere as the variable
*name* is still the same. When forming variables in **GML** it must have
a name that starts with a letter or the underscore symbol "\_" and can
contain only letters, numbers, and the underscore symbol '\_' with a
maximum length of 64 symbols. So, valid variables are things like fish ,
foo_bar , num1 , or \_str , while invalid variables would be 6fish , foo
bar , or \*num . Now, In many programming languages you need to create a
variable "assignment" before you can use it. This basically means that
you tell the computer the name you wish to use for the variable and
assign it an initial value. The variable is then given a place in memory
to store the value or perform operations on it. Assigning a variable
takes the form of:

``` gml
&amp;lt;variable&amp;gt; = &amp;lt;expression&amp;gt;;
```

An expression can be a simple value but can also be more complicated,
so, rather than assigning a value to a variable, one can also add a
value to the current value of the variable using **+=** , for example:

``` gml
a = 100;   // Assigning a simple value
b = 200;
c = 300;
a += b;    // Assigning with operation
a = b + c; // Assigning with expression
```

NOTE The GameMaker Language will also accept " := " for assignments,
although this is not typically the most common way to do it:

``` gml
&amp;lt;variable&amp;gt; := &amp;lt;expression&amp;gt;;
```

Similarly, you can subtract using **-=** , multiply using **\*=** ,
divide using **/=** , or use bitwise operators using **\|=** , **&=** ,
or **^=** . You can also add or subtract *one* from a value using **++**
, **--** . For further information see the section on [Expressions And
Operators](Expressions_And_Operators) . Note that you *cannot* do
the following (or any variation):

``` gml
a = b = c = 4;
```

And instead it should be done as:

``` gml
a = 4;
b = 4;
c = 4;
```

The variable assignments shown above are all **instance** variables,
however there are actually three other main variable categories when you
program with GameMaker and each has its own **scope** (which can be
considered as its area of operation, or reach). The different kinds of
variables and their scope are all outlined in the following pages:

-   [Local Variables](Variables/Local_Variables)
-   [Instance Variables](Variables/Instance_Variables)
-   [Global Variables](Variables/Global_Variables)
-   [Constants](Variables/Constants)

The GameMaker Language also has multiple different built-in variables
that can have any of the above mentioned scopes (except *local* ). These
variables are special as they are included by default as part of the
objects and the rooms in the game world. Some built in global variables
are listed in the section mentioned above, and the different parts of
the manual for sprites, rooms, objects, etc... also outline the built-in
variables available in each case. Examples of such built-in instance
variables would be:

-   
    [sprite_index](../GML_Reference/Asset_Management/Sprites/Sprite_Instance_Variables/sprite_index)
-   [ path_scale
    ](../GML_Reference/Asset_Management/Paths/Path_Variables/path_index)
-   [ speed
    ](../GML_Reference/Asset_Management/Instances/Instance_Variables/speed)

And examples of built-in global variables would be:

-   [ view_xport
    ](../GML_Reference/Cameras_And_Display/Cameras_And_Viewports/view_xport)
-   [ GM_version ](../GML_Reference/OS_And_Compiler/GM_version)
-   [ room ](../GML_Reference/Asset_Management/Rooms/room)

Most built-in variables can be changed and set like other variables, and
some can even be [arrays](Arrays) , only you don't have to set them
to create them like you would a regular variable as they will already be
initialised to a default value. Finally, there are a number of functions
that are dedicated to setting, getting or checking variables in some
way, available from the following page:

-   [Variable
    Functions](../GML_Reference/Variable_Functions/Variable_Functions)
