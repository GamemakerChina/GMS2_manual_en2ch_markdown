# json_decode

### **IMPORTANT!** This function - while still valid - has been superseded by the function  [json_parse()](json_parse)  , and we recommend that you only use this function for legacy support.

JSON (JavaScript Object Notation) is a lightweight data-interchange
format which is easy for to read and write, for both people and
machines. It is built on two basic structures:

-   A collection of name/value pairs, called a [ DS Map
    ](../../Data_Structures/DS_Maps/DS_Maps) in GameMaker but also
    known as a "dictionary" or "object".
-   An ordered list of values, called a [ DS List
    ](../../Data_Structures/DS_Lists/DS_Lists) in GameMaker but this
    can also be called an "array" or "sequence".

With this function, you can decode a piece of JSON and convert it into a
DS Map , ready for use in GameMaker . If the JSON to be decoded requires
a hierarchy of lists and maps within the central DS map, these are
decoded too and also created for you, using the following rules (note
that these rules apply to the top-level structure only):

-   ***JSON is a single value*** - returns a DS map with a single entry
    "default" that is the value
-   ***JSON is an array of objects or values*** - returns a DS map with
    a single entry "default" that is a DS list of the objects or values
-   ***JSON is an object*** - returns a DS map that has the object
    entries in it

**NOTE** : When decoding JSON arrays, there is a map with the key
"default" ONLY when an array is the top level structure, and ONLY for
that top-level array. Internal lists decode directly to DS map without
being enclosed in a DS map. **NOTE** : If you wrote GameMaker arrays
into the top level, or as the contents of a DS map or DS list, these
will be decoded as DS lists, **not** arrays. Normally you would know
what keys the JSON decodes to, but if not then you can use the [
ds_map_size() ](../../Data_Structures/DS_Maps/ds_map_size) , [
ds_map_find_first()
](../../Data_Structures/DS_Maps/ds_map_find_first) and [
ds_map_find_next() ](../../Data_Structures/DS_Maps/ds_map_find_next)
functions to parse the map and get the necessary information. **NOTE** :
GameMaker creates the necessary DS maps and lists from the JSON, and for
cleaning up you only need to delete the **top level** map or list and
GameMaker will automatically delete from memory all the maps and lists
underneath. **NOTE** : This function allows you to load JSON files with
a maximum nesting limit of 128. **IMPORTANT** : You cannot have 64bit
numbers in your JSON, as they will not work correctly due them not being
handled by the JSON format.

#### Syntax:

``` gml
json_decode(string)
```

|          |                                                                           |                                                                          |
|----------|---------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                              |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The JSON format string that you are passing to the function for decoding |

#### Returns:

``` gml
 DS Map ID

or -1 (if it fails)
```

#### Example:

``` gml
var resultMap = json_decode(requestResult);
var list = ds_map_find_value(resultMap, "default");
var size = ds_list_size(list);
for (var n = 0; n &amp;lt; ds_list_size(list); n++;)
{
    var map = ds_list_find_value(list, n);
    var curr = ds_map_find_first(map);
    while (is_string(curr))
    {
        global.Name[n] = ds_map_find_value(map, "name");
        curr = ds_map_find_next(map, curr);
    }
}
ds_map_destroy(resultMap);
```

The above code will decode a JSON string and parse it to generate a
global array.
