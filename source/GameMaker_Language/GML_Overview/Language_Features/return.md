# return

The return statement has the following syntax:

``` gml
return (&amp;lt;expression&amp;gt;)
```

You only use the return statement in [script
functions](../Script_Functions) and
[methods](../Method_Variables) , and it is used to return a value
from the function to be used in further code or function calls. It
should be noted that the *execution of the function ends at the return
statement* , meaning that any code which comes after return has been
called will not be run. Here is a short example script called sqr_calc
which calculates the square of whatever value is passed to it, and it
includes error catching in case the parameter that it is passed is not a
real number:

``` gml
/// @function            sqr_calc(val);
/// @param {real}  val   The value to calculate the square of
/// @description         Calculate the square of the given value

function sqr_calc(value)
{
    if !is_real(value)
    {
        return 0;
    }
    else
    {
        return (value * value);
    }
}
```

To call a function from within a piece of code, just use it the same way
as when calling runtime functions - that is, write the function name
with the parameter values in parentheses. So, the above function would
be called like this:

``` gml
if keyboard_check_pressed(vk_enter)
{
    val = scr_sqr(amount);
}
```

Here the variable val will either be 0 (because the variable amount is
not a real number) or the total for value \* value .
