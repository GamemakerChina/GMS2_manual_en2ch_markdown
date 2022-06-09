# network_destroy

With this function you can remove a network socket connection from your
game. **NOTE** : This function will not work when used in a project
running on the HTML5 target.

#### Syntax:

``` gml
network_destroy(socket);
```

|          |                                                                                                          |                                 |
|----------|----------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                     | Description                     |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The id of the socket to remove. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !os_is_network_connected()
{
    network_destroy(sock);
}
```

The above code will check to see if there is a data connection and if
none is found, destroy the socket with the id "sock".
