# math_get_epsilon

This function will return the current epsilon value for the target
platform. For more information on epsilon, please see the function [
math_set_epsilon() ](math_set_epsilon) .

#### Syntax:

``` gml
math_get_epsilon();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var e = math_get_epsilon();
if e != 0.000001
{
    math_set_epsilon(0.000001);
}
```

This will retrieve the current epsilon value and store it in a local
variable, which is then checked and a new epsilon set if required.
