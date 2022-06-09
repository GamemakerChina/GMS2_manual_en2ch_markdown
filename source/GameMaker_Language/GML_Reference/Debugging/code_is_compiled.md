# code_is_compiled

This function will return true if the platform compiles outside of the
virtual machine, such as for the YYC and JS platforms.

#### Syntax:

``` gml
code_is_compiled();
```

#### Returns:

``` gml
 Boolean
```

#### **Example:**

``` gml
if code_is_compiled()
{
    show_debug_message("Compiler okay!");
}
```

The above code checks to see if the game was compiled using the YoYo
Compiler and shows a debug message if it was.
