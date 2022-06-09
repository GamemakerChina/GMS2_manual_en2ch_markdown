# parameter_string

Command-line parameters are those extra commands that you can add to an
exe to change how the program is run and with this function you can get
the chosen command-line parameter as a string. You can find the number
of parameters for the current game using the function [
parameter_count() ](parameter_count) , where the first parameter has
index 1 and the last one has the index returned by the function (a value
of 0 is special on that it is the filename of the game executable,
including the path). It should be noted that this function will work for
on the HTML5 platform, retrieving the url parameters.

#### Syntax:

``` gml
parameter_string(n);
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var p_num;
p_num = parameter_count();
if p_num &amp;gt; 0
{
    var i;
    for (i = 0; i &amp;lt; p_num; i += 1)
    {
        p_string[i] = parameter_string(i + 1);
    }
}
```

The above code will get the number of command-line parameters, and if
there is 1 or more it will loop through them and store them as strings
in an array.
