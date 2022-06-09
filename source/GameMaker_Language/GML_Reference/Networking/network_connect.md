# network_connect

With this function you can send a request to connect to a server. The
function takes the *socket id* to connect through (see [
network_create_socket() ](network_create_socket) ) and requires you
to give the IP address to connect to (a string) as well as the port to
connect through, and if the connection fails a value of less than 0 will
be returned. The connection uses a special protocol that ensures only
GameMaker games connect to each other, however if you need to connect to
a server that is not a GameMaker game, you can use [
network_connect_raw() ](network_connect_raw) . Note that by default
the function is synchronous, meaning that your game may appear to "hang"
as the connection is made. You can set a timeout value for connection,
or alternatively make the creation asynchronous, using the function
[network_set_config()](network_set_config) , or alternatively use
the function [network_connect_async()](network_connect_async)
instead. NOTE You cannot use this function on HTML5. For WebSockets, use
the [Async function](network_connect_async) .

#### Syntax:

``` gml
network_connect(socket, url, port);
```

|          |                                                                                                          |                                         |
|----------|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                     | Description                             |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The id of the socket to use.            |
| url      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The URL or IP to connect to (a string). |
| port     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The port to connect to.                 |

#### Returns:

``` gml
 Real

or

 Network Socket ID
```

#### Example:

``` gml
client = network_create_socket(network_socket_tcp);
network_connect(client, "192.134.0.1", 6510);
```

The above code will create a new TCP socket then attempt to connect
through that to the given IP address on port 6510.
