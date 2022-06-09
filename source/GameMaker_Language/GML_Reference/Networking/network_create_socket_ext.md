# network_create_socket_ext

This function is used to create a new client socket for your game to
communicate over the network. You must define the socket type (see the
list of constants below) and give a port to use, and the function will
return a unique *id* which should be used in all further function calls
for that socket, or a value of less than 0 if the connection fails.

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
network_create_socket_ext(protocol, port);
```

|          |                                                                                                             |                             |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                        | Description                 |
| protocol |  [Socket Type Constant](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The network protocol to use |
| port     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                         | The port to use             |

#### Returns:

``` gml
 Network Socket ID
```

#### Example:

``` gml
client = network_create_socket_ext(network_socket_udp, 6510);
```

The above code will create a new UDP socket on port 6510.
