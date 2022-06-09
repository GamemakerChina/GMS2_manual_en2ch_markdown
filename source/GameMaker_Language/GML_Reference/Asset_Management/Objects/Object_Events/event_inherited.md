# event_inherited

This function will call the current event of the parent object of the
instance. Normally, when an instance has a parent object, it
automatically inherits all the same events as the parent, but if (for
example) your parent object has a create event and you add one to your
child object, all instances of the child object will run the new create
event that you have added and *not* that which is in the parent object.
Should you need to use both the parent object event and the child object
event of the same type, you should use this function as it will run the
parent object event before continuing with the rest of the code or
actions that the child event contains.

#### Syntax:

``` gml
event_inherited();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
event_inherited();
switch (sprite_index)
{
    case spr_Enemy_1: dmg += 2; break;
    case spr_Enemy_4: dmg -= 1; break;
    case spr_Enemy_10: dmg +=10; break;
}
```

The above code calls the inherited parent event (in which we initialise
the variable " dmg ") and then goes on to modify the " dmg " variable.
If there is no parent specified for the instance running this code, we
would get an "unknown variable" error as dmg has not been defined.
