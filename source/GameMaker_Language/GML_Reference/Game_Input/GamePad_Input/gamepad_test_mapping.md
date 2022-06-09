# gamepad_test_mapping

This function can be used to set the gamepad mapping on those targets
that permit it. You supply the "slot" index for the gamepad to set, and
then the map string, which should have been created using the SDL format
with the following fields:

``` gml
&amp;lt;guid&amp;gt;,&amp;lt;description&amp;gt;,platform:&amp;lt;platform-name&amp;gt;,&amp;lt;bindings&amp;gt;
```

The details that should be included in each of these fields are:

-    guid  - a string of digits and letters that uniquely identifies a
    device type (this can be retrieved using the [ gamepad_get_guid()
    ](gamepad_get_guid) function)
-    description  - an Ascii description of the device (this can be
    retrieved using the [ gamepad_get_description()
    ](gamepad_get_description) function)
-    platform-name  - will be either "platform:android",
    "platform:windows", "linux", or "mac" (note that **this will be
    appended automatically onto the string when you call this function**
    , and so you do not need to supply it when constructing your own
    mapping strings)
-    bindings  - a set of entries separated by a ',' to bind actual
    input to specific GML constants

The comma separated list of entries follows a specific format for each
entry:

``` gml
&amp;lt;abstract-gp-name&amp;gt;:&amp;lt;value-binding&amp;gt;
```

Here (ie: the direct gamepad input) can be any one of the following:

-    a  - This represents an axis of the gamepad, where the is one of
    the axis from 0 to [ gamepad_axis_count() ](gamepad_axis_count)
    -1
-    b  - This represents a button of the gamepad, where the is one of
    the buttons from 0 to [ gamepad_button_count()
    ](gamepad_button_count) -1
-    h.  - This represents a hat of the gamepad, where the represents a
    hat from 0 to [ gamepad_hat_count() ](gamepad_hat_count) -1, and
    the will be either 1, 2, 4, or 8.

Each input value should be bound to an SDL name, which is expressed as
\<\>abstract-gp-name\> , which in turn is bound to a GML constant. The
table below shows the equivalence between the SDL name and the GameMaker
constant:

|                 |               |
|-----------------|---------------|
| SDL Name        | GML Name      |
|  a              | gp_face1      |
|  b              | gp_face2      |
|  x              | gp_face3      |
|  y              | gp_face4      |
|  leftshoulder   | gp_shoulderl  |
|  lefttrigger    | gp_shoulderlb |
|  rightshoulder  | gp_shoulderr  |
|  righttrigger   | gp_shoulderrb |
|  guide          | gp_select     |
|  start          | gp_start      |
|  leftstick      | gp_stickl     |
|  rightstick     | gp_stickr     |
|  dpup           | gp_padu       |
|  dpdown         | gp_padl       |
|  dpleft         | gp_padr       |
|  dpright        | gp_padd       |
|  leftx          | gp_axislh     |
|  lefty          | gp_axislv     |
|  rightx         | gp_axisrh     |
|  righty         | gp_axisrv     |

When you have constructed your mapping string it should look something
like this:

``` gml
"050000005e040000fd020000ffff3f00,Xbox Wireless Controller,a:b0,b:b1,start:b4,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,dpup:h0.1,guide:b6,leftshoulder:b9,leftstick:b7,lefttrigger:a4,leftx:a0,lefty:a1,rightshoulder:b10,rightstick:b8,righttrigger:a5,rightx:a2,righty:a3,x:b2,y:b3,platform:android"
```

#### Syntax:

``` gml
gamepad_test_mapping(index, mapping_string);
```

|                |                                                                           |                                                                   |
|----------------|---------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument       | Type                                                                      | Description                                                       |
| index          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | Which gamepad index "slot" to set.                                |
| mapping_string |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The map string to use (see the description for more information). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var mapping = gamepad_get_guid(global.padIndex) + "," + gamepad_get_description(global.padIndex);
var len = array_length(global.PadInstances);
for (i = 0; i &amp;lt; len; i += 2)
{
    var left = global.PadInstances[i];
    var right = global.PadInstances[i+1];
    mapping += "," + left.sdlLabel + ":" + right.binding;
}
gamepad_test_mapping(global.padIndex, mapping);
```

The above code will loop through a number of instances and use the
values of different variables that they contain to create a mapping
string, which is then set for use on the gamepad in the given slot
index.
