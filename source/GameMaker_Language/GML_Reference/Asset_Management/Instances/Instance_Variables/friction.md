# friction

Friction is one of the "built in" properties that instances can have and
can be used to slow the instance down over time when the [ speed
](speed) is other than zero. It works simply by subtracting an
amount from the speed every step until the object has a speed of 0, so
if the friction is set to, for example, 0.1 and the speed of the
instance is 1 (1 pixel per step), it will slow down and stop after 10
steps have passed. Note too that the friction is applied to positive and
negative speeds equally with the net result always being that the object
has a speed of 0 after a given time.

#### Syntax:

``` gml
friction;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if abs(speed) &amp;gt; 0
{
    friction = 0.05;
}
else
{
    friction = 0;
}
```

The above code will only apply friction if the instance's absolute speed
is above 0.
