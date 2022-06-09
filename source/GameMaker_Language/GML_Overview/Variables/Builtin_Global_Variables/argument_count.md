# argument_count

This **read-only** variable returns the number of "arguments" that are
passed through to a [script function](../../Script_Functions) or a
[method](../../Method_Variables) . Normally used in conjunction with
an argument array ( [ argument\[0...15\] ](argument) ) to permit
varying input arguments for a given function. **NOTE** : This isn't
strictly required any more and is provided for legacy support more than
anything else. All user-defined functions will accept variable
arguments, and any argument passed into a function that is not part of
the named inputs will be initialised to undefined by default, which can
be checked using the
[is_undefined()](../../../GML_Reference/Variable_Functions/is_undefined)
function.

#### Syntax:

``` gml
argument_count;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
function my_array()
{
    var i, arg;
    for (i = 0; i &amp;lt; 5; i += 1;)
    {
        if argument_count &amp;gt; i
        {
            arg[i] = argument[i]
        }
        else
        {
            arg[i] = -1;
        }
    }
}
```

The above code uses the argument_count variable along with the argument
array to initialize variables, and is an example of how to permit a
user-defined function to accept a variable number of arguments.
