# try / catch / finally

The try , catch and finally statements can be used in your game for
error checking and permit you to test out blocks of code and control
what happens if any [runtime
exceptions](../../../Additional_Information/Errors/Runner_Errors)
occur. Using these will prevent the exception ending the game and
showing the standard error message to the user, but this means that you
will have to handle what happens next in that case, like saving out log
files - for example - and ending the game gracefully (note that if you
choose to do nothing, your game may become unstable and not perform
correctly). At it's most basic the try syntax is as follows:

``` gml
try
{
    &amp;lt;statement1&amp;gt;;
    &amp;lt;statement2&amp;gt;;
    ...
}
```

However, having a try without anything to actually handle any exceptions
the code may produce will not be very helpful, so we usually pair it
with a catch , with the following syntax:

``` gml
try
{
    &amp;lt;statement1&amp;gt;;
    &amp;lt;statement2&amp;gt;;
    ...
}
catch(&amp;lt;variable&amp;gt;)
{
    &amp;lt;statement1&amp;gt;;
    &amp;lt;statement2&amp;gt;;
    ...
}
```

What catch does is permit you to run extra code supplied in the
following block when an exception from the previous try has been caught.
If this is a runtime exception, then the supplied variable can be used
to access a [struct](../Structs) which will contain the following
information:

``` gml
{
message : "",               // a string that is a short message for this exception
longMessage : "",           // a string that is a longer message for this exception
script : "",                // a string that describes where the exception came from
stacktrace : [ "", "" ],    // an array of strings that is the stack frame the exception was generated
}
```

A simple example of use is shown below:

``` gml
var a = 0, b = 0, c = 0;
try
{
    c = a div b;
}
catch( _exception)
{
    show_debug_message(_exception.message);
    show_debug_message(_exception.longMessage);
    show_debug_message(_exception.script);
    show_debug_message(_exception.stacktrace);
}
```

It may be that you want to run some code regardless of whether an
exception was thrown or not, and so for that you can add in a finally
block. The finally syntax is:

``` gml
finally
{
    &amp;lt;statement1&amp;gt;;
    &amp;lt;statement2&amp;gt;;
    etc...
}
```

It is worth noting that you can have any combination of these together,
ie:

-    try / finally
-    try / catch
-    try / catch / finally

Note that within the finally block you *cannot* use [ break ](break)
, [ continue ](continue) , [ exit ](exit) or [ return
](return) statements as they have no meaning in this context and the
compiler will generate an error if they are used. Finally, you can also
nest various try / catch / finally within each other, for example:

``` gml
var a = 0, b = 0, c = 0;
try
{
    try
    {
        c = a div b;
    }
    finally
    {
        ++a;
    }
}
catch(_exception)
{
    ++a;
    show_debug_message(_exception.message);
    show_debug_message(_exception.longMessage);
    show_debug_message(_exception.script);
    show_debug_message(_exception.stacktrace);
}
finally
{
    show_debug_message("a = " + string(a));
}
```

It is worth noting that you can take over the default GML error message
and use your own handler code by calling the function [
exception_unhandled_handler()
](../../GML_Reference/Debugging/exception_unhandled_handler) . This
[runtime function](../Runtime_Functions) permits you to supply a
custom [method](../Method_Variables) to use that will be called
whenever any unhandled exceptions occur in your game.
