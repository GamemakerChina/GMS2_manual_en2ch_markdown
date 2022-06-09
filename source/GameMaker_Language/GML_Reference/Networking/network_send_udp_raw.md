# network_send_udp_raw

With this function you can send data over the network using UDP to a
server. The function takes the *socket id* to connect through, the URL
to connect to and the port to use. You must then supply the *buffer id*
which contains the data to be sent (for more information on buffers see
[Reference - Buffers](../Buffers/Buffers) ) and finally the size (in
bytes) of the data. UDP is "connectionless" in that you don't actually
do a connect, you just send a packet directly to an IP, and the server
gets incoming data from an IP address and has to deal with it "as is".
The data sent is not formatted by GameMaker in any way and the receiving
devices will get the data as a stream which means you will have to
handle it yourself. The function will return the number of bytes of data
sent, or a number less than 0 if the send has failed. NOTE This function
will not work when used in a project running on the HTML5 target, and
neither will HTML5 projects be able to receive UDP.

#### Syntax:

``` gml
network_send_udp_raw(socket, url, port, bufferid, size);
```

|          |                                                                                                          |                                            |
|----------|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                     | Description                                |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)  | The id of the socket to use.               |
| url      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The url or IP to connect to (a string).    |
| port     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The port to connect to.                    |
| bufferid |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                     | The id of the buffer to get the data from. |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The size (in bytes) of the data.           |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
network_send_udp_raw(sock, "www.macsweeneygames.com", 6510, buff, buffer_tell(buff));
```

The above code will send a raw UDP packet to the server defined by the
URL on the port 6510. The data is taken from the buffer indexed in the
variable "buff".
