# path_position

This function can be used to get or to set the position of an instance
along a path. The value is normalised from 0 - 1, so if you set it to,
for example, 0.5, the instance will be moved to exactly the middle of
the path.

#### Syntax:

``` gml
path_position;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
path_position = random(1);
```

The above code sets the instance to a random position anywhere on the
current path.
