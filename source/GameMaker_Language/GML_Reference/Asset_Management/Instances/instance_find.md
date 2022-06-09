# instance_find

All instances have a unique identifier ( [ id
](Instance_Variables/id) ) which can be used to modify and
manipulate them while a game is running, but you may not always know
what the id for a specific instance is and so this function can help as
you can use it to iterate through all of them to find what you need. You
specify the object that you want to find the instance of and a number,
and if there is an instance at that position in the instance list then
the function returns the id of that instance, and if not it returns the
special [keyword](../../../GML_Overview/Instance_Keywords) **noone**
. You can also use the keyword **all** to iterate through all the
instances in a room, as well as a parent object to iterate through all
the instances that are part of that parent / child hierarchy, and you
can even specify an instance (if you have its id ) as a check to see if
it actually exists in the current room. Please note that as instances
are sorted in an *arbitrary* manner, there is no specific order to how
the instances are checked by this function, and any instance can be in
any position. The maximum value for "n" in this function would be

-   For the keyword **all** : [ instance_count - 1 ](instance_count)
-   For an object index: [ instance_number(OBJ) - 1
    ](instance_number)

#### **Syntax:**

``` gml
instance_find(obj, n);
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects)           | The object to find the nth instance of |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of the instance to find.    |

#### Returns:

``` gml
 Instance ID

or

 noone
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; instance_number(obj_Enemy); ++i;)
{
    enemy[i] = instance_find(obj_Enemy,i);
}
```

The above code will use a for loop to iterate through all the instances
of "obj_Enemy" and store their **id** in the array "enemy\[\]".
