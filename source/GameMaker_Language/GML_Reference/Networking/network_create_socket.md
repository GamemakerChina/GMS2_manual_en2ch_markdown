# network_create_socket

This function is used to create a new client socket for your game to
communicate over the network. You must define the socket type (see the
list of constants below) and the function will return a unique *id* for
that socket, which should be used in all further function calls for that
socket, or a value of less than 0 if the connection fails. TIP You can
use the IP "127.0.0.1" to connect back to the same device that is
running the game.

|                                                                                                             |                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
|  [Socket Type Constant](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  |                                                                                                                                       |
| Constant                                                                                                    | Description                                                                                                                           |
|  network_socket_tcp                                                                                         | Create a socket using TCP.                                                                                                            |
|  network_socket_udp                                                                                         | Create a socket using UDP.                                                                                                            |
|  network_socket_ws                                                                                          | Create a WebSocket using TCP. ( ***NOTE** : Use [Async](network_connect_raw_async) functions for connecting through WebSockets* ) |
|  network_socket_wss \*                                                                                      | Create a secure WebSocket using TCP.                                                                                                  |

NOTE 1 It is also possible to secure your simple WebSocket (
network_socket_ws ) by using the wss:// protocol in your URLs. NOTE 2 \*
Secure WebSockets will not work on UWP and Xbox One when using the
legacy XDK platform, however they will work on those targets when using
GDK.

#### Syntax:

``` gml
network_create_socket(type);
```

|          |                                                                                                             |                                                                           |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                               |
| type     |  [Socket Type Constant](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The type of socket connection to create (see the constants listed above). |

#### Returns:

``` gml
 Network Socket ID
```

#### Example:

``` gml
if os_browser == browser_not_a_browser
{
    client = network_create_socket(network_socket_tcp);
    network_connect( client, "192.134.0.1", 6510 );
}
else
{
    client = network_create_socket(network_socket_ws);
    network_connect_raw_async( client, "192.134.0.1", 6520 );
}
```

The above code will check whether the game is running in a browser or
not and create a new TCP or Web socket before attempting to connect
through that to the given IP address on the given port.
