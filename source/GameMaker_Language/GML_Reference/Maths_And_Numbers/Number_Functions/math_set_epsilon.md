# math_set_epsilon

Epsilon is a value used to determine whether two numbers subject to
rounding error are close enough to be considered "equal". It is useful
when dealing with floating point maths as it can reduce the "rounding
errors" that make certain operations return values that appear incorrect
or contrary to what we expect. For example, we may have added a value to
the image index of a sprite and expect the result to be a single
integer, but due to the nature of floating point maths, the actual final
value ends up being something like 5.0000002, so when we have the
following check:

``` gml
if image_index == 5
{
    //do something
}
```

The code does not behave as expected and returns false . However, if we
set the epsilon value to 0.000001, the image_index value will be rounded
to the nearest real number that is +/- 0.000001 of the original value,
making the above comparison return true. The epsilon value will be used
for all the following integer
[operators](../../../GML_Overview/Expressions_And_Operators) :

-    \< : Less than
-    \> : Greater than
-    == : Equal to
-    \<= : Less than or equal to
-    \>= : Greater than or equal to
-    != : Not equal to

Note that setting an epsilon value of 0 will disable all rounding, and
using a value of 1 will give an error.

#### Syntax:

``` gml
math_set_epsilon(epsilon);
```

|          |                                                                         |                                                |
|----------|-------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                    | Description                                    |
| epsilon  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new epsilon value (from 0 to 0.999999999). |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
math_set_epsilon(0.0001);
```

This will set the epsilon value for all further floating point
operations.
