# network_resolve

This function will return the IP address of the given URL.

#### Syntax:

``` gml
network_resolve(url);
```

|          |                                                                        |                                      |
|----------|------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                   | Description                          |
| url      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The URL to get the IP of (a string). |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
game_ip = network_resolve("www.macsweeneygames.com");
```

The above code will return the IP address of the given URL and store it
in the variable "game_ip".
