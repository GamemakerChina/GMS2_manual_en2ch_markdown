# sprite_get_name

This function will return the name *as a string* of the specified
sprite. This name is the one that has been specified for the sprite in
the resource tree of the main GameMaker window. Please note that this is
*only* a string and cannot be used to reference the sprite directly -
for that you would need the *sprite index* . You can, however, use this
string to get the *sprite index* using the returned string along with
the function [ asset_get_index()
](../../Assets_And_Tags/asset_get_index) .

#### Syntax:

``` gml
sprite_get_name(index);
```

|          |                                                                   |                                             |
|----------|-------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                              | Description                                 |
| index    |  [Sprite Asset](../../../../../../The_Asset_Editors/Sprites)  | The index of the sprite to get the name of. |

#### Returns

``` gml
 String
```

#### **Example:**

``` gml
str = sprite_get_name(sprite_index);
```

The above code will get the name of the sprite index for the instance
running the code and store the return value in the variable "str".
