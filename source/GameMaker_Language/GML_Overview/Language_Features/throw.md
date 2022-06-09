# throw

The throw runtime statement permits you to generate your own [runtime
exceptions](../../../Additional_Information/Errors/Runner_Errors) ,
ending the game and showing an error message, using the following
syntax:

``` gml
throw (&amp;lt;expression&amp;gt;);
```

The expression used can be a value or a string or any other data type,
and this will then generate an exception error which is - by default -
shown on the screen and on closing the error message the game will end.
For example calling this:

``` gml
throw ("Hello World!");
```

will cause the following unhandled exception error to be shown:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Overview/ThrowUnhandledMessage.png)  
You can, however, take over this error message and use your own handler
code by calling the function [ exception_unhandled_handler()
](../../GML_Reference/Debugging/exception_unhandled_handler) . This
[runtime function](../Runtime_Functions) permits you to supply a
custom [method](../Method_Variables) to use that will be called
whenever any unhandled exceptions occur in your game.
