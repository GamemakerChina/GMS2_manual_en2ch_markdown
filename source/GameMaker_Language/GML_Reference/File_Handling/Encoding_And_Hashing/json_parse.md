# json_parse

This function can be used to parse a JSON string (either previously
created using [json_stringify](json_stringify) or from any valid
source), and convert it into a collection of arrays or structs, where an
array is the equivalent of a JSON array and a struct is the equivalent
of a JSON object. You supply the string to parse, and the function will
return the top level array or struct which can then be used in your
code. If you are not sure of the contents of the JSON, you can use the
different [Variable
Functions](../../Variable_Functions/Variable_Functions) (like [
typeof() ](../../Variable_Functions/typeof) and [
variable_struct_get_names()
](../../Variable_Functions/variable_struct_get_names) in case of a
struct) to check the returned contents. Note that trying to parse
an invalid value (i.e.: not a string) will throw an exception error.
When using this function there are some important things to note:

-   If the supplied JSON string includes undefined as a value for any
    property, it will be converted to pointer_null upon being parsed.
-   This function only allows you to load JSON files with a maximum
    nesting limit of 128.

#### Syntax:

``` gml
json_parse(json)
```

|          |                                                                           |                          |
|----------|---------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                      | Description              |
| json     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The JSON string to parse |

#### Returns:

``` gml
 Struct

or

 Array
```

#### Example:

``` gml
json = "{\"myObj\": { \"apples\":10, \"oranges\":12, \"potatoes\":100000, \"avocados\":0 }, \"myArray\":[0, 1, 2, 2, 4, 0, 1, 5, 1]}";

data = json_parse(json);
show_debug_message(data);
```

The above code creates a new string containing a valid JSON object, and
then calls json_parse() to convert that string into a GML struct. It
then prints the result to the debug log. NOTE You will notice that the
JSON string contains a backslash ( \\ ) before every double quote ( " )
inside it: json = "{ **\\"** myObj This is to ensure that the double
quote is read as an actual character within the string, instead of being
read as part of the code and closing the string prematurely. This way we
are using a backslash to "escape" the double quote. If you are loading
JSON from an external file however, there is no need to escape
characters in that file and doing so may result in errors during
parsing.

------------------------------------------------------------------------

After parsing the JSON string above, if you know its structure, you can
use various [Variable
Functions](../../Variable_Functions/Variable_Functions) to check and
read its contents:

``` gml
data = json_parse(json);

// Check if the struct has myObj variable
if variable_struct_exists(data, "myObj")
{
    // Check if it's a struct
    if is_struct(data.myObj)
    {
        // Print all struct members to the log
        var _names = variable_struct_get_names(data.myObj);
        var _str = "";
        for (var i = 0; i &amp;lt; array_length(_names); i++;)
        {
            _str = _names[i] + ": " + string(variable_struct_get(data.myObj, _names[i]));
            show_debug_message(_str);
        }
    }
}

// Check if the struct has myArray variable
if variable_struct_exists(data, "myArray")
{
    // Check if it's an array
    if is_array(data.myArray)
    {
        show_debug_message(data.myArray);
    }
}
```

The above code will parse the given JSON string, generating the
following console output:

``` gml
oranges: 12
potatoes: 100000
avocados: 0
apples: 10
[ 0,1,2,2,4,0,1,5,1 ]
```
