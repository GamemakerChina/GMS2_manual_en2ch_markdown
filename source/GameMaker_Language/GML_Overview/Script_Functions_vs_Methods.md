# Script Functions vs. Methods

This page covers essential information about using script functions vs.
methods.

## Basic Difference

A [script function](Script_Functions) is created with this syntax:

``` gml
function name()
{
    code;
}
```

A [method variable](Method_Variables) is created with this syntax:

``` gml
name = function()
{
    code;
}
```

You should use the first syntax in scripts, to create global functions
that can be called from any scope in your game. You should use the
second syntax when creating functions in
[structs/constructors](Structs) and objects. This syntax creates a
variable containing a method.

## Direct Calls

You can call both script functions and methods directly by using
parentheses () ,  just like a [runtime function](Runtime_Functions)
:

``` gml
// Create the function
function reset_x()
{
    x = xstart;
}

// Call the function
reset_x();
```

You can also use the function [ script_execute()
](../GML_Reference/Asset_Management/Scripts/script_execute) to run a
script function, although it's now a legacy function and not recommended
for use.

## Indirect Calls: Methods

You can store a reference to a method, in another variable, to call it
later through that different variable:

``` gml
// Create method
reset_alpha = function()
{
    image_alpha = 1;
}

// Pass reference and call
temp_1 = reset_alpha;
temp_1();
```

NOTE See how the code doesn't put () after reset_alpha . That's because
we're reading the method reference and not calling it. In this example,
calling temp_1 will call reset_alpha , as it stores a reference to that
**method** . You are completely fine to pass around a method reference
in this way. When using script functions though, there is a caveat.

## Indirect Calls: Script Functions

You can also store a reference to a script function, in another
variable:

``` gml
// Create function
function reset_x()
{
    x = xstart;
}

// Store reference
temp_1 = reset_x;
```

Now, you can call temp_1 by doing this:

``` gml
temp_1();
```

However, since this variable refers to a **script function** , it first
has to convert it into a **method** , and then call it. This can easily
result in increased memory usage, especially if you're calling it every
frame, because the engine now has to create a new method every frame for
this call. So, what is the solution?

-   Use [ script_execute()
    ](../GML_Reference/Asset_Management/Scripts/script_execute) to
    call the script function via its reference, which will not create a
    method.
-   Or, the better solution: convert your script function [into a
    method](../GML_Reference/Variable_Functions/method) when passing
    its reference.

To implement the second solution, your code would look like this:

``` gml
temp_1 = method(undefined, reset_x);
```

This is creating a new method from the reset_x script function, using [
method() ](../GML_Reference/Variable_Functions/method) . Calling
temp_1() now using parentheses will not increase memory usage, as the
method is already created for you. Again, this only applies if you're
calling a script function **indirectly** , via a reference stored in a
variable. Calling it directly doesn't cause such problems.
