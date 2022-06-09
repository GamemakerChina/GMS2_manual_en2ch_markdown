# Structs & Constructors

A **struct** is a variable that holds a collection of other variables.
The variables that a struct holds can be of any [data
type](Data_Types) previously mentioned and these variables can be
read from and written to after the initial struct declaration, and you
can also add more variables to a struct after it has been declared. The
variables used in a struct should follow the usual variable naming
scheme, i.e.: they cannot start with a number and should only be made up
of alphanumeric characters and the underscore "\_" character, and also
note that the contents of a struct are *independent of the instance or
function that created it* , and as such you can - if you wish -
use built-in variable names such as image_index or x and y . After the
initial creation, structs have no processing overhead while they exist,
although they *will* take up space in memory. The struct syntax is as
follows:

``` gml
 &amp;lt;variable&amp;gt;

=
{

 &amp;lt;variable&amp;gt;

:

 &amp;lt;value&amp;gt;

,

 &amp;lt;variable&amp;gt;

:

 &amp;lt;value&amp;gt;

,
    etc...
};
```

So, an example of this in practice would be:

``` gml
mystruct =
{
    a : 20,
    b : "Hello World"
};
```

The above code creates an instance scope struct in the variable mystruct
and populates it with some values (structs can be created at local,
instance and global scopes, just like any other variable - see the
section on [Variables and Variable
Scope](Variables_And_Variable_Scope) for more information). Note
that you don't have to populate the contents of a struct when it is
created initially and you can create an empty struct by simply doing
this:

``` gml
mystruct = {};
```

This struct can then be added to at a later point in the game code. Here
is an example of a struct with various variables and data types:

``` gml
var _xx = 100;
mystruct =
{
    a : 10,
    b : "Hello World",
    c : int64(5),
    d : _xx + 50,
    e : function(a, b)
        {
            return a + b;
        },
    f : [ 10, 20, 30, 40, 50 ],
    g : image_index
};
```

You'll notice in the above code that you can also define methods and use
runtime functions in structs, and you can also use local and instance
variables within the struct declaration.

### Instance Variables in Struct Declaration?

For example, you'll notice in the above example that the struct variable
"g" is being set to image_index , which is an instance variable. You
might think that you'd need to use the [keyword](Instance_Keywords)
other in this case to get the instance variable, but this is not
necessary. Essentially, when you define a struct **, all member
variables on the left-hand side of the colon ":" are the *struct*
variables, and the values and variables on the right-hand side use the
scope of whatever is defining the struct** (in this case, an instance).
Let's look at a simple example to illustrate this. Say you want to
define a struct with the variables "x" and "y" and you want to set them
to the "x" and "y" of the instance defining the struct. In practice the
code would look like this:

``` gml
mystruct =
{
    x : x,
    y : y
};
```

In the above code the struct member variables x and y are being set to
the values held in the instance variables x and y , since the right-hand
side of the colon ":" refers to the instance that is defining the
struct. It is worth noting that this means you *cannot* use struct
member variables for defining subsequent variables within the struct
declaration. For example, the following would give you an error:

``` gml
mystruct =
{
    a : 10,
    b : 10,
    c : a + b
}
```

The error occurs because the variables a and b are actually being
evaluated at the scope of whatever is defining the struct (they are on
the right-hand side of the colon ":"), and are *not* the ones being
defined within the struct itself.

### ***IMPORTANT!*** You **cannot** use any built-in ***global*** scope variables as struct member names, eg:  game_id  or  fps  . You can find a full list of these global variables from the following page:

-   [Struct Forbidden Variables](Struct_Forbidden_Variables)

Once a struct has been defined, you can access the data within it using
the "point" notation, like this:

``` gml
mystruct =
{
    a : 20,
    b : "Hello World"
}

mystring = mystruct.b + string(mystruct.a);
```

You can also perform operations on the variables within a struct or use
them in functions, just as you would with any other variable. For
example:

``` gml
mystruct.a += 1;
mystruct.b = mystruct.a + 20;
mydir = point_direction(mouse_x, mouse_y, mystruct.xx, mystruct.yy);
```

Finally, structs can have other structs nested inside them, like this:

``` gml
mystruct =
{
    a :
    {
        aa : "This is an example"
    },
    b :
    {
        bb : "And another one"
    },
};
```

To access such nested structs you would still use the point notation,
like this:

``` gml
var _str = mystuct.a.aa + " " + mystruct.b.bb;
show_debug_message(_str);
```

Another way to access data in a struct is by using the [ with()
](Language_Features/with) function. So, for example, you could do
this:

``` gml
with(mystruct)
{
    a += other.x;
}
```

Using with() changes the scope of the code to the given struct where you
can manipulate the member variables at the struct scope. Note that in
the example we also use the [ other keyword](Instance_Keywords) .
This works just like in an instance when using with() and will reference
the instance (or struct) that is actually running the code block. When a
struct is no longer required it can be removed from memory using the [
delete ](Language_Features/delete) operator, which flags the struct
as being able to be garbage collected. This is not strictly required as
the garbage collector may do this automatically if the struct is no
longer referenced in your code, but it is good practice to do so and we
recommend it (for example, call delete in the [Clean Up
event](../../The_Asset_Editors/Object_Properties/Object_Events) of
an instance to explicitly tell the garbage collector that an instance
scope struct is to be deleted). Here is an example:

``` gml
// Create event
mystruct =
{
    pos_x : x,
    pos_y : y,
    count : 1000
};

// Clean Up event
delete mystruct;
```

## Constructor Functions

You can also use [script functions](Script_Functions) or
[methods](Method_Variables) to create functions that can be used to
generate new structs, which requires the use of the constructor keyword
for the function and the [ new ](Language_Features/new) operator
when creating a struct from such a function. See the following function:

``` gml
function Vector2(_x, _y) constructor
{
    x = _x;
    y = _y;

    static Add = function(_vec2)
    {
        x += _vec2.x;
        y += _vec2.y;
    }
}
```

Or, using the method variable syntax:

``` gml
Vector2 = function(_x, _y) constructor
{
    x = _x;
    y = _y;

    static Add = function(_vec2)
    {
        x += _vec2.x;
        y += _vec2.y;
    }
}
```

Here we are creating a function called Vector2 and telling GameMaker
that this is a function used for creating structs by adding the
constructor keyword after its definition. You can then call this
constructor function like this:

``` gml
v2 = new Vector2(10, 10);
```

The variable v2 will now contain a struct with the variables x and y and
the [static](Functions/Static_Variables) [method
variable](Method_Variables) Add . You can also make use of optional
arguments in your constructor functions:

``` gml
function Vector2(_x = 0, _y = 0) constructor
{
    x = _x;
    y = _y;
}
```

This constructor will now use 0 for the \_x and \_y arguments if they
are not specified when the function is called. This means that you can
create a new Vector2 struct without having to specify any arguments:

``` gml
empty_vector = new Vector2();
```

## Inheritance

Functions created this way will also support single **inheritance** ,
ie: you can create a constructor function that inherits data from
another constructor function. **NOTE** : When working with inheritance,
you cannot use method variables to define the constructor function, only
script functions. For example, we created the Vector2 constructor
function above, so we can then use that as the "parent" for another
constructor function, which we'll call Vector3 :

``` gml
function Vector3(_x, _y, _z) : Vector2(_x, _y) constructor
{
    z = _z;

    static Add = function( _vec3 )
    {
        x += _vec3.x;
        y += _vec3.y;
        z += _vec3.z;
    }
}
```

As you can see, when defining the function we use a colon " : " to
separate the new constructor from the parent constructor to be inherited
from. The child constructor ( Vector3 ) passes the \_x and \_y arguments
into the parent ( Vector2 ) constructor, which are used to run the
parent's constructor first, after which the child's constructor is
executed. This way the child constructor gets the parent's variables ( x
and y ) and can also define its own ( z ). You can also pass constant
values into the parent constructor, so that a certain child constructor
always provides the same values to its parent constructor:

``` gml
function Item(damage) constructor
{
    my_damage = damage;
}

function BasicSword() : Item(10) constructor
{}

var _basic_sword = new BasicSword();
show_debug_message(_basic_sword.my_damage); // Prints 10
```

This means that the damage of a basic sword will always be 10 , since it
passes that value to its parent constructor irrespective of what its own
arguments might be. Note that assigning a default value to an argument
in a child constructor will override the parent's default value for that
argument. See the following example:

``` gml
function Parent(value = 10) constructor
{
    show_debug_message(value);
}

function Child(value = 20) : Parent(value) constructor
{
    show_debug_message(value);
}

var _child = new Child();
```

Both of these constructors will print 20 to the output log, as that was
the default value for the argument set by the child constructor, and the
same value was passed into the parent constructor. For more details on
the new and delete operators, please see the following pages:

-   [ new ](Language_Features/new)
-    [ delete ](Language_Features/delete)

## String Output

One final thing to mention about structs is that you can change what is
output to the console from them for debugging. By default, calling the
function [ show_debug_message()
](../GML_Reference/Debugging/show_debug_overlay) on a struct will
output the contents of the struct (as shown above). However, it's
possible to customise this message by adding a specifically named method
to the struct called toString :

``` gml
mystruct =
{
    a : 20,
    b : "Hello World",

    toString : function()
    {
        return "This stuct says " + b + ", " + string(a) + " times!";
    }
}
show_debug_message(mystruct);
```

Now when the show_debug_message() function is called, the toString
method will be used to generate the output and - with the above
example - you'll get:

``` gml
This struct says Hello World, 20 times!
```

Note that you can also call the [ string()
](../GML_Reference/Strings/Strings) function on a struct reference
and use that to display the contents - or the toString method - to the
screen, or save it to a file, or whatever, eg:

``` gml
var _str = string(mystruct);
draw_text(32, 32, _str);
```

Finally, there are a number of runtime functions that you can use on
structs to get the variables they contain as well as a few other things.
You can find them in the following section:

-   [Variable
    Functions](../GML_Reference/Variable_Functions/Variable_Functions)
