# Constants

A constant is a type of variable that is set once at the start of the
game and then never changes. In fact, constant values *cannot be changed
after they have been declared* . This makes them ideal for holding
values that are used throughout the game to identify special data. In
the GameMaker Language there are two types of user-defined constant:
**macros** and **enums** , both of which are explained below. Also note
that any value that is always the same is classed as a constant,
regardless of the [data type](../Data_Types) , for example, a string
or the number 3. NOTE The GameMaker Language also has a number of
built-in constant values that are used to identify specific things.
These are outlined on the appropriate pages for the runtime functions
that require them in the [GML
Reference](../../GML_Reference/GML_Reference) section.

## Macros

While not exactly variables, macros are similar to them in how they are
used, i.e.: they are named values that you can use throughout your code
to replace hard-coded values. Basically, a macro is a named variable
that holds an expression. You can define your own macros using the
[Script Editor](../Script_Functions) and then use them in your code
and actions as if they were regular variables, with the one difference
being that they *can't be changed in the game* . The syntax structure
for a macro is as follows:

``` gml
#macro

 &amp;lt;variable&amp;gt;


 &amp;lt;expression&amp;gt;
```

For example, say you define the following macro " total_weapons ":

``` gml
#macro total_weapons 10
```

Macro syntax... The syntax shown above must be used correctly to define
macros. You cannot use an equal sign (like in variables) or put a
semicolon at the end (like in a regular statement). Doing so will cause
your macro definition to become invalid. For example, this is not the
correct way to define a macro: \#macro total_weapons = 10; Removing the
equal sign and colon will make it a valid macro definition. You could
then use this in your code like this:

``` gml
pos++;

if (pos &amp;gt;= total_weapons)
{
    pos = 0;
}
```

Note that you would not be able to change the constant's value, so code
like this will cause the game to crash:

``` gml
total_weapons = 11;
```

You can define a macro anywhere in your code or in a script and it will
be *pre-compiled* and included in your game as if it was there from the
start, but we recommend that you create a dedicated script asset and
define all your macros in there. It will be easier to organise and debug
later! If you need the value of a macro to change at run-time then you
should probably make it a [global variable](Global_Variables) ,
since these can be changed from code during a game, unless you set the
macro to be a [runtime](../Runtime_Functions)
[function](../Runtime_Functions) . By setting the macro to a
function it means that this function will be called every time you use
the macro. For example:

``` gml
#macro col make_colour_hsv(irandom(255), 255, 255)
```

You would then call this macro something like this:

``` gml
image_blend = col;
```

Using this code will make the image blend a different colour every time
the macro is used. It is worth noting that you can also split macros
over multiple lines using the \\ character to show where the line
breaks. An example would be something like:

``` gml
#macro hello show_debug_message("Hello" + \
string(player_name) + \
", how are you today?");
```

This is purely cosmetic, in that splitting a macro like this will have
no effect over the result of the final macro when used, and is simply to
provide support for multi-line text on macros that have longer lines of
code. One very important feature of macros is that they can be defined
for use with specific
[Configurations](../../../Settings/Configurations) (configs),
meaning you can have the same macro name but give it different values
based on the currently selected config. For example, say you have a
configuration for Android Ads and another for iOS Ads, then you could
define a single macro to hold the required app ID value:

``` gml
#macro ad_id "";
#macro Android:ad_id "com.yoyogames.googlegame"
#macro iOS:ad_id "com.yoyogames.appstoregame"
```

As you can see, you give the config name first then a colon : and then
the macro name and value. Note that you cannot have any white-space
between the colon : and either the config name nor the macro name
otherwise you will get an error.

## Enums

An enum is an "enumerator", and it essentially permits you to create
your own limited data type with a list of constant values, and they have
the following structure:

``` gml
enum

 &amp;lt;variable&amp;gt;

{

 &amp;lt;constant&amp;gt;

[=

 &amp;lt;value&amp;gt;

],

 &amp;lt;constant&amp;gt;

[=

 &amp;lt;value&amp;gt;

],
    // etc...
}
```

In the following example, we create an enum for the colours of the
rainbow and assign it various constants and default values:

``` gml
enum rainbowcolours
{
    red,
    orange,
    yellow,
    green,
    blue,
    indigo,
    violet
}
```

The enum entries can only be **integer numbers** or **expression s with
previous enums that evaluate to an integer number** , and by default are
numbered from 0 upwards, so our example given above would default to red
= 0 , orange = 1 , yellow = 2 , etc... You can also assign values to the
enum variables at the time of creation:

``` gml
enum enum_test
{
    val = 10;
}

enum rainbowcolours
{
    red = 5,
    orange = 5 * 2,
    yellow = 15,
    green = 20,
    blue = 25,
    indigo = 30,
    violet = 35 * enum_test.val
}
```

Notice in the above example we use another enum to create an expression
for "violet". This only works if the enum being referenced was created
*before* the enum that is using it in an expression, but it will not
work for variables or functions, since the enum value must be able to be
evaluated as a constant when the project is Compiling . Also note that
all enum values evaluate to **integer** values, and when you create your
own you should be aware that *only integer values are permitted* for
enums to work. This value can be any integer number that a floating
point double precision number can represent, including negative values.
To later access the value within a given enum type, you can use the
point "." method, like this:

``` gml
variable = &amp;lt;enum_name&amp;gt;.&amp;lt;

 enum_variable

&amp;gt;;
```

As an example, let's use the " rainbowcolours " enum that we created in
the code above:

``` gml
colour_value = rainbowcolours.green * rainbowcolours.red;
```

The colour_value variable would now hold the value 100 (20 \* 5). Note
that you *cannot* modify the values for any enum constant after it has
been created, much the same as you can't modify macros after they have
been created. **NOTE** : Enum values are stored as int64s, so running
[is_real()](../../GML_Reference/Variable_Functions/is_real) on them
will return false .

## Built-In Constants

The following table shows a list of the built-in constants that can be
returned by some functions and operations in your projects:

|                   |                                                                                                                                                                                                               |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Constant          | Description                                                                                                                                                                                                   |
|  pointer_null     | This constant indicates that the pointer is not pointing to anything meaningful (the same as NULL in C++ or null in C#). This value is falsy .                                                                |
|  pointer_invalid  | This constant simply means that the value is not a valid pointer                                                                                                                                              |
|  undefined        | This constant is returned when a function has to return *something* but has no appropriate or "correct" value to return. This value is falsy .                                                                |
|  NaN              |  This constant that can be returned when the compiler cannot evaluate the results of an operation as a number - for example, 0 / 0 cannot be defined as a real number, and is therefore represented by NaN    |
|  infinity         |  This constant refers to a number that is considered infinite, such as the result you would get when dividing any floating point value by zero, eg: 1.0/0.                                                    |
|  true             | This constant represents the value 1, which is what GameMaker will evaluate as a boolean "true" (note that any value equal to or greater than 1 will evaluate as true ).                                      |
|  false            | This constant represents the value 0, which is what GameMaker will evaluate as a boolean "false" (note that any value less than or equal to 0 will evaluate as false ).                                       |
|  pi               | This constant represents the value of pi: 3.141592653589793280 etc... although the exact value will depend on various factors like the OS or the platform being targeted.                                     |

See [Equality Table](../../../Additional_Information/Type_Tables#h)
for information on equality comparisons for a few of the constants
listed above.
