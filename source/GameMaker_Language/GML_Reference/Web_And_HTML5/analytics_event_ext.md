# analytics_event_ext

This function will send the specified text to the analytics provider
that you have set up through the [HTML5 Game
Options](../../../Settings/Game_Options/HTML5) . This function can
be used to create a custom analytic to track something outside of the
scope of the provider being used, and will also accept custom
parameter/value pairs, where the parameter is a string and the value a
real number. For Google Analytics, you can only add in one extra pair
while Flurry will accept up to 7.

#### Syntax:

``` gml
analytics_event_ext(string, string_param, value);
```

|                      |                                                                        |                                             |
|----------------------|------------------------------------------------------------------------|---------------------------------------------|
| Argument             | Type                                                                   | Description                                 |
| string               |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | A string to send to the provider.           |
| string_param\[0 -9\] |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The parameter to send (a string).           |
| value\[0 - 9\]       |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The value of the parameter (a real number). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var num, time; ini_open("Options.ini");
 num = ini_read_real("Data", "Plays", 0); num += 1; time = current_time; analytics_event_ext(GAME_NAME, "Plays", num, "Time", time); ini_write_real("Data", "Plays",
num); ini_close();
```

The above code will get play information from an ini file as well as the
current time and then send those details to the analytics provider.
