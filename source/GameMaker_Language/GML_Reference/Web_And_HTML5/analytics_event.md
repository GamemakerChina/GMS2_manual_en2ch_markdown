# analytics_event

This function will send the specified text to the analytics provider
that you have set up through the [HTML5 Game
Options](../../../Settings/Game_Options/HTML5) . This function can
be used to create a custom analytic to track something outside of the
scope of the provider being used.

#### Syntax:

``` gml
analytics_event(string);
```

|          |                                                                        |                                  |
|----------|------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                   | Description                      |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | A string to send to the provider |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if hs_new
{
    analytics_event("New hiscore of " + string (score));
}
```

The above code will check a variable to see if it is true and if it is
then a special analytics event will be triggered with the specified
string.
