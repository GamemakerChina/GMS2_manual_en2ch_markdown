# os_is_network_connected

With this function you can check and see if your device currently has an
internet connection and it will return true if it does, or false if it
does not, and depending on the OS, it may attempt to make a connection
before returning a value. The function has an optional argument to
enable/disable it attempting to make a connection when called, and this
option is curently **only** for the Nintendo Switch target. When set to
true the funtion will attempt to make a connection, and when set to
false it will simply be limited to checking the connection. Note that
attempting to make a connection may cause the Switch OS to hang for a
few seconds. ** NOTE ** This function checks the internal device API
that controls connections and so may return true if there is a bluetooth
connection, a Wi-Fi connection, or even just a normal network connection
that permits internet access.

#### Syntax:

``` gml
os_is_network_connected([attempt_connection]);
```

|                    |                                                                         |                                                                                                                   |
|--------------------|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Argument           | Type                                                                    | Description                                                                                                       |
| attempt_connection |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL For the Nintendo Switch target **only** . Set to true to attempt an OS level connection when called.    |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if os_is_network_connected()
{
    global.connected = true;
}
```

The above code checks to see if the device has a connection to the
internet and if so it sets a global variable.
