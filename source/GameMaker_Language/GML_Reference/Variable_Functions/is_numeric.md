# is_numeric

This function returns whether a given variable is a numeric value (real,
int32, int64 or boolean) or not. In some cases you want to check and see
if a variable in GameMaker holds any numeric value, and that's when you
would use this function. The function will return true if the given
input is numeric, and false otherwise.

#### Syntax:

``` gml
is_numeric(n);
```

|          |                                                                                   |                     |
|----------|-----------------------------------------------------------------------------------|---------------------|
| Argument | Type                                                                              | Description         |
| n        |  [Variable](../../../../GameMaker_Language/GML_Overview/Data_Types#variable)  | The input to check. |

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
if is_numeric(val)
{
    current_val += val;
}
```

The above code checks the variable "val" to see if it is a numeric value
and if it is it then adds it to the given variable.
