# time_source_get_children

For the given Time Source , this function returns an array containing
the [Time Source
ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)
s of its children.

#### Syntax:

``` gml
time_source_get_children(id);
```

|          |                                                                                                      |                                          |
|----------|------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                 | Description                              |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to get the children of   |

#### Returns:

``` gml
 Array

of

 Time Source ID
```

#### Example:

``` gml
var _children = time_source_get_children(time_source);
var _count = array_length(_children);

for (var i = 0; i &amp;lt; _count; i ++)
{
    time_source_destroy(_children[i]);
}

time_source_destroy(time_source);
```

This code goes through all the children of a Time Source , and destroys
them one-by-one. At the end, it destroys the parent Time Source . This
is necessary for destroying parent Time Source s, as you cannot destroy
a Time Source that has existing children.
