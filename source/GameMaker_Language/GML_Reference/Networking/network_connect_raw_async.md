# network_connect_raw_async

With this function you can send a request to connect to a server. The
function takes the *socket id* to connect through (see [
network_create_socket() ](network_create_socket) ) and requires you
to give the IP address to connect to (a string) as well as the port to
connect through, and if the connection fails a value of less than 0 will
be returned. The difference between this function and [
network_connect_async() ](network_connect_async) is that this
function can connect to any server and does nothing to the raw data,
meaning that you have to implement the protocols yourself at the server
end. Note that this function is asynchronous, generating an
[Asynchronous
Networking](../../../The_Asset_Editors/Object_Properties/Async_Events/Networking)
event of the type network_type_non_blocking_connect .

#### Syntax:

``` gml
network_connect_raw_async(socket, url, port);
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
```

#### Example:

``` gml
client = network_create_socket(network_socket_tcp); network_connect_raw_async(client, "www.macsweeneygames.com", 6510);
```

The above code will create a new TCP socket then attempt to create a
"raw" asynchronous connection through that to the given URL on port
6510.
