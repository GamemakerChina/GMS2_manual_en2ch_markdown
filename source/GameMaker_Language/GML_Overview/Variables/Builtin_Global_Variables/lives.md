# lives

This variable is **global** in scope and is used to hold a numeric value
which is usually used for the player lives. This variable is only
designed to support legacy projects from previous versions of
*GameMaker* and should ***not be used in new projects*** as it may be
deprecated in the future.

#### Syntax:

``` gml
lives;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example

``` gml
if (lives &amp;lt; 5)
{
    lives += 1;
}
```

The above code checks the lives variable and if it is less than 5, 1 is
added to it.
