# tag_get_assets

With this function you can retrieve the names of all assets that have
been assigned the given tag or tags. You supply either a single tag
string or an [array](../../../GML_Overview/Arrays) , where each item
in the array is a tag string. The function will return an array where
each entry is the name (as a string) of the asset with the given tag. If
you need the unique index for the asset, then you can use the function [
asset_get_index() ](asset_get_index) along with the returned name.
If there are no assets with the given tag(s), or if there is an error
(eg: the given tags do not exist), then an empty array will be returned.

#### Syntax:

``` gml
tag_get_assets(tags);
```

|          |                                                                                                                                                              |                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                                                                                                         | Description                                                    |
| tags     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Array](../../../../../GameMaker_Language/GML_Overview/Arrays) of Strings    | A single asset tag string or an array with various asset tags. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
backgrounds = ds_list_create();
var _assets = tag_get_assets("background");
for (var i = 0; i&amp;lt; array_length(_assets); ++i;)
{
    if asset_get_type(_assets[i]) == asset_sprite
    {
        ds_list_add(backgrounds, asset_get_index(_assets[i]));
    }
}
```

The above code creates a list, then retrieves the names of all the
assets with the tag "background". It loops through the array of names
returned, checking to see if any of them are sprite assets, and if they
are then the unique index value for the asset is added to the list for
future use.
