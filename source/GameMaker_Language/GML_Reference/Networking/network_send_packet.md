# network_send_packet

With this function you can send a data "packet" through the network. The
function takes the *socket id* to connect through and then you must
supply the *buffer id* which contains the data to be sent (for more
information on buffers see [Reference - Buffers](../Buffers/Buffers)
) and finally the size (in bytes) of the data packet. Packets sent with
this function are formatted such that the GameMaker game receiving the
data can "split" the packets correctly, and the function will return the
number of bytes of data sent, or a number less than 0 if the send has
failed. It is worth noting that the final size of the data being sent
that is returned by this function will also include the GameMaker header
information, which is an additional 12 bytes.

#### Syntax:

``` gml
network_send_packet(socket, bufferid, size);
```

|          |                                                                                                          |                                            |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                     | Description                                |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The id of the socket to use.               |
| bufferid |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                     | The id of the buffer to get the data from. |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The size (in bytes) of the data.           |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
buff = buffer_load("player_save.dat");
network_send_packet(sock, buff, buffer_get_size(buff));
```

The above information loads a previously saved buffer data into memory
and returns the buffer id to be stored in the variable "buff". This
complete buffer is then send as a packet over the network using the
socket identified by the variable "sock".
