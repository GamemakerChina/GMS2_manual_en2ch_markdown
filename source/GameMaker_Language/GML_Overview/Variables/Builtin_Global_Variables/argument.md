# argument

This variable holds an [array](../../Arrays) that is used along with
the read-only variable [argument_count](argument_count) in [script
functions](../../Script_Functions) or
[methods](../../Method_Variables) . Each array position holds an
input value for the function and is specifically for use with *variable*
argument functions. Note that there are also a series of independent
global scope variables that can also be used in user-defined functions
to reference the different input arguments: argument0 , argument1 ,
argument2 , etc... up to argument15 . **NOTE** : This isn't strictly
required any more and is provided for legacy support more than anything
else. All user-defined functions will accept variable arguments, and any
argument passed into a function that is not part of the named inputs
will be initialised to undefined by default, which can be checked using
the
[is_undefined()](../../../GML_Reference/Variable_Functions/is_undefined)
function.

#### Syntax:

``` gml
argument[

 n

]
argument1
argument2
...
argument15
```

#### Returns:

``` gml
 Variable

(can be of any data type supplied to the function)
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
