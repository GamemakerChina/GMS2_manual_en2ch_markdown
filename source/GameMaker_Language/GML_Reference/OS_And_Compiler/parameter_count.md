# parameter_count

Command-line parameters are those extra commands that you can add to an
exe to change how the program is run. You can find the number of
parameters for the current game using this function, where the first
parameter has index 1 and the last one has the index returned by the
function (a value of 0 is special on that it is the filename of the game
executable, including the path). It should be noted that this function
will work for on the HTML5 platform, retrieving the url parameters.

#### Syntax:

``` gml
parameter_count();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
p_num = parameter_count();
```

The above code will store the number of command-line parameters that
have been used for the game in the variable "p_num".
