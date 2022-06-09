# network_send_broadcast

With this function you can broadcast the data from a buffer locally to a
range of IP addresses (for more information on buffers see [Reference -
Buffers](../Buffers/Buffers) ). The range is limited to that of the
device running the server, such that if the device has an IP of
92.168.11.130, then the data will be broadcast over the range
92.168.11.\*. The function will return the number of bytes of data sent,
or a number less than 0 if the send has failed. **NOTE** : This function
will only work when used with UDP - your server needs to be TCP and your
client needs to have a UDP client socket created with [
network_create_socket_ext() ](network_create_socket_ext) in order to
receive any broadcasts sent from the server. **NOTE** : This function
will not work when used in a project running on the HTML5 target.

#### Syntax:

``` gml
network_send_broadcast(socket, port, bufferid, size);
```

|          |                                                                                                          |                                            |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                     | Description                                |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The id of the socket to use.               |
| port     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The port that the server will use.         |
| bufferid |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                     | The id of the buffer to get the data from. |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The size (in bytes) of the data.           |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
buffer_seek(broadcast_buffer, buffer_seek_start, 0);
buffer_write(broadcast_buffer, buffer_string, global.ServerName);
network_send_broadcast(server, 6511, broadcast_buffer, buffer_tell(broadcast_buffer));
```

The above code writes the name string of the current server (stored in
"global.ServerName"), then writes it to a binary buffer with the id
"broadcast_buffer". This data is then broadcast locally to a range of
IPs (the device IP is currently implied as the broadcast base range) to
port 6511.
