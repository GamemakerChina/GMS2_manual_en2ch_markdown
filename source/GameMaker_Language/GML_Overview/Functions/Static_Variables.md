# Static Variables

An interesting feature of [script functions](../Script_Functions)
and [method variables](../Method_Variables) is that they can have
**static variables** . A static variable is one that is defined the
first time that the function is called and that will maintain its value
from then onward. To create a static variable you need to define it
using the static keyword, as shown in this simple example:

``` gml
counter = function()
{
    static num = 0;
    return num++;
}
```

In the above example, the variable num is a static variable, and so will
be defined as 0 the first time the function is called, but every time
the function is called after that, the variable initialization will be
ignored. So, if you then call this function like this:

``` gml
for (var i = 0; i &amp;lt; 10; ++i;)
{
    show_debug_message(counter());
}
```

The output will be:

``` gml
0
1
2
3
4
5
6
7
8
9
```

If you didn't use the static keyword here then the output would simply
be 0 for every iteration of the loop, since the variable num will be
getting defined as 0 every time the function is called before being
returned. Note that a static variable can only be changed inside the
original function, and returning it will simply give you a copy of its
value - essentially the shared static variable can only be changed by
the function that contains it. A static variable is always initialized
at the top of the function, so no matter where you define a static
variable in the function, it will always be available to be read and
changed throughout the function (even if it's used before being
defined). See the following example:

``` gml
function add_health()
{
    my_health++;
    show_debug_message(my_health);
    static my_health = 1;
}
```

Here the static variable " my_health " is being changed and printed to
the compiler output *before* being initialized. While that looks wrong,
it is perfectly fine because static variables are initialized *before*
any function code is executed. Note that if there are multiple static
variables in a function, the order in which they were defined will be
kept when they are initialized at the top. You can also use the static
keyword within a function to create a **static function** , which - like
with variables - simply means that the function will only be defined
once, which is the first time the function is called, for example:

``` gml
function(_x, _y) Vector2 constructor
{
    x = _x;
    y = _y;

    static Add = function( _other )
    {
        x += _other.x;
        y += _other.y;
    }
}
```

In the above example, the constructor function Vector2 can be used to
create a struct, and the struct will have some variables, one of which
is the method variable Add . Since this variable has been defined as
static, the function it contains will only be initialized *once* the
first time the Vector2 function is called, and all further structs
created with this constructor will reference the function Add that was
created initially, instead of creating a new function for each struct
(for more information on structs and the constructor keyword please see
[here](../Structs) ). When using inheritance with constructors, any
static variables in the child constructor will only be initialized once
the parent constructor has been executed, so the child constructor's
static variables will not override the parent's static variables. See
the following example:

``` gml
function Parent() constructor
{
    show_debug_message(value);
    static value = 10;
}

function Child() : Parent() constructor
{
    show_debug_message(value);
    static value = 20;
}

var _child = new Child();
```

Calling the Child() constructor prints this to the output log:

``` gml
10
20
```

The first value is from the parent constructor, and the second is from
the child constructor. This shows that the child's static variable value
was not initialized until the parent constructor was finished, and that
in each constructor the static variable was initialized before the
show_debug_message() call.
