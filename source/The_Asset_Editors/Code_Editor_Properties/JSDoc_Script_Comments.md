# JSDoc Script Comments

If you wish your custom functions to have code completion and to show
the required arguments in a specific manner in the code editor, then you
need to add some [JSDoc
style](https://www.oracle.com/technical-resources/articles/java/javadoc-tooll)
comments. These comments are used to tell the auto-complete feature how
the function should be used and filled out in the [script
editor](../Scripts) . The format for a typical function header would
be to have the function name, the description of the function, and then
the list of the different arguments (parameters) that the function
takes, making sure to start each line with a triple backslash " /// " as
that tells GameMaker to parse the comment as being JSDoc style. The
comments themselves need to be given an identifier (preceded by " @ ")
and content, and the available identifiers are as follows:

|                                 |                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Identifier                      | Content                                                                                                              |
|  @function / @func              | The full function name and arguments for the function, eg: my_func(x, y, colour) .                                   |
|  @description / @desc           | A general description of what the function does.                                                                     |
|  @param / @arg / @argument      | The argument type (optional), enclosed in {} , the argument name, and a short description (with spaces in between)   |

To get an idea of how this would work when writing your own functions,
let's take this basic example:

``` gml
function is_same_object(_id, _obj) {
     if (_id.object_index == _obj)     {         return true;     }     else return false; }
```

All this script does is check to see if an instance has the same
object_index as a given object and would be called simply as:

``` gml
if is_same_object(id, obj_Player) {
     instance_destroy() }
```

However, writing that into the code editor will show you the argument
variable names directly ( \_id and \_obj ) which in most cases is not
very descriptive. You can use JSDoc to define custom argument names and
descriptions, along with information for the function as well:

``` gml
/// @function                is_same_object(id, object) /// @description             Compare an instance index with an object index. /// @param {real} inst_id    The unique instance ID value of the instance to check. /// @param {real}
object_id  The object index to be checked against.
 function is_same_object(_id, _obj) {
     if (_id.object_index == _obj)     {         return true;     }     else return false; }
```

Now, when calling this function anywhere in your project, you will see
the new argument names that were entered in the JSDoc comments:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/JavaDoc_Example.png)  
In the image above, the top part shows the function in the auto-complete
and the bottom part shows how the argument helper at the bottom works.
Note that both the optional "type" and the obligatory "description"
parts of @param are not displayed by default in the IDE code complete,
and to see them you must activate the options in the [GML
Preferences](../../Setting_Up_And_Version_Information/IDE_Preferences/GML_Code_Preferences)
. You can wrap an argument name in \[\] brackets to indicate that it is
optional. The code editor will then expect any number of arguments
between the minimum required arguments and the total number of
arguments. For example, see the following function:

``` gml
/// @function    animate_position(end_x, end_y, start_x, start_y) /// @desc        Animates the instance to ending point, from optional starting point /// @arg end_x /// @arg end_y /// @arg [start_x] /// @arg [start_y]
 function animate_position (x1, y1, x2, y2) {
     // Function code }
```

The start_x and start_y arguments are marked as optional, which means
the code editor will now expect 2 to 4 arguments, as can be seen in the
warning message:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/JavaDoc_Optional.png)  
**NOTE** : You will get the same behaviour if you use optional arguments
in the function declaration. See [script
functions](../../GameMaker_Language/GML_Overview/Script_Functions)
for more information. Since scripts can have multiple functions in them,
you can add JSDoc comments for each of them before its declaration:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Additional_Information/JavaDoc_MultipleFunctions.png)  
