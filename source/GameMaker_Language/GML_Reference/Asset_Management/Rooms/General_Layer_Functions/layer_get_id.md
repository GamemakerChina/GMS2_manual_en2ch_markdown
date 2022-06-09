# layer_get_id

This function can be used to get the unique ID value for a given
**layer** . In the IDE, all layers have a name and a type, and to be
able to edit or change them through code you must give the **layer ID**
value. This function is used to retrieve this ID by using the name (a
string) of the layer (as written in the IDE). If you create a new layer
through code using the function [ layer_create() ](layer_create)
then that function will return the unique ID value instead (dynamical
created layers do not get names). Note that if you give the name of a
layer that does not exist in the current room, then you will get an
error and the project will crash.

#### Syntax:

``` gml
layer_get_id(layer_name)
```

|            |                                                                              |                                  |
|------------|------------------------------------------------------------------------------|----------------------------------|
| Argument   | Type                                                                         | Description                      |
| layer_name |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the layer (a string) |

#### Returns:

``` gml
 Layer ID

or -1 (if the layer specified doesn't exist)
```

#### Example:

``` gml
var near = instance_nearest(x, y, obj_Tree);
var layer_id = layer_get_id("Instances Front");
layer_add_instance(layer_id, near);
```

The above code will first get the index of the nearest instance to the
given x/y position and store it in a local variable. It then gets the
unique instance layer ID for the layer named "Instances Front", and
moves the found instance onto that layer.
