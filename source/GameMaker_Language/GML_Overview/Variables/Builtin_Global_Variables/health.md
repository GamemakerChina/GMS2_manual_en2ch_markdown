# health

This variable is **global** in scope and is used to hold a numeric value
which is usually used for the player health. This variable is only
designed to support legacy projects from previous versions of
*GameMaker* and should ***not be used in new projects*** as it may be
deprecated in the future.

#### Syntax:

``` gml
health;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example

``` gml
if (health &amp;lt;= 0)
{
    global.state = "Game Over";
    instance_destroy();
}
```

The above code checks the health variable and if it is less than or
equal to 0, a global variable is set and the instance is destroyed.
