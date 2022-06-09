# json_encode

### **IMPORTANT!** This function - while still valid - has been superseded by the function  [json_stringify()](json_stringify)  , and we recommend that you only use this function for legacy support.

JSON (JavaScript Object Notation) is a lightweight data-interchange
format which is easy for to read and write, for both people and
machines. It is built on two basic structures:

-   A collection of name/value pairs, called a [ DS Map
    ](../../Data_Structures/DS_Maps/DS_Maps) in GameMaker but also
    known as a "dictionary" or "object" in other programming languages.
-   An ordered list of values, called a [ DS List
    ](../../Data_Structures/DS_Lists/DS_Lists) in GameMaker but this
    can also be called an "array" or "sequence" in other programming
    languages.

json_encode() takes a DS map or array that you have previously created
and encodes it as a JSON string which you can then use as (for example)
part of an [ http_post_string()
](../../Asynchronous_Functions/HTTP/http_post_string) call, or - so
it can be stored externally - it can be written to a file. If using an
array as the top level structure, then the array can only contain valid
values or other arrays, and *not* data structures. For that you should
use the appropriate DS functions. **IMPORTANT!** JSON is agnostic about
numbers. In any programming language, there can be a variety of number
types of various capacities and complements, fixed or floating, binary
or decimal. That can make interchange between different programming
languages difficult. JSON instead offers only the representation of
numbers that humans use: a sequence of digits. All programming languages
know how to make sense of digit sequences even if they disagree on
internal representations. For more information see the [ECMA JSON
Standard](http://www.ecma-international.org/publications/standards/Ecma-404)
. Note that care should be taken when writing JSON to an ini file, as
the ini specifications can cause issues when using quotes and escape
characters. See the function [ ini_write_string()
](../Ini_Files/ini_write_string) for more information. Also note
that if you encode an int64 to JSON it will write it as an *int* if it
is in the valid range for an int32, as a *double* if it can do so
without losing precision or (if neither of those cases is applicable) as
a *string* with an identifier " @i64@ " before it and " $i64$ " after
it. When you come to decode the JSON to a map again GameMaker will pick
these identifiers up and re-convert the value to an int64. This does
mean that if the JSON is intended for a server or some other
non-GameMaker target, these values will not be appropriate and so should
be avoided. **NOTE** : The hierarchical functionality of JSON is
available through special DS map and DS list functions (for example
[ds_map_add_list()](../../Data_Structures/DS_Maps/ds_map_add_list)
or
[ds_list_mark_as_map()](../../Data_Structures/DS_Lists/ds_list_mark_as_map)
), so you are able to encode sub-lists and maps.

#### Syntax:

``` gml
json_encode(map)
```

|          |                                                                                                          |                                                       |
|----------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                                     | Description                                           |
| map      |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | A DS map with the information to encode (or an array) |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var hiscore_map, i, str;
hiscore_map = ds_map_create();
for (i = 0; i &amp;lt; 10; i ++;)
{
    ds_map_add(hiscore_map, name[i], score[i]);
}
str = json_encode(hiscore_map);
get[0] = http_post_string("http://www.angusgames.com/game?game_id=" + string(global.game_id), str)
ds_map_destroy(hiscore_map);
```

The above code creates a DS map and then loops through the name and
score arrays, adding each key/value pair to the new map. Next, this map
is encoded using json_encode() and stored as a string in the variable
"str". This string is then sent to a web server using http_post_string()
and the DS map is destroyed to prevent a memory leak as it is no-longer
needed.
