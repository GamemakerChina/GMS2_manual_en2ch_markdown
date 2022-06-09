# network_send_raw

With this function you can send a "raw" data packet through the network.
The function takes the *socket id* to connect through and then you must
supply the *buffer id* which contains the data to be sent (for more
information on buffers see [Reference - Buffers](../Buffers/Buffers)
) and finally the size (in bytes) of the data packet. The data sent is
not formatted by GameMaker in any way and the receiving devices will get
the data as a stream which means you will have to handle it yourself.
The function will return the number of bytes of data sent, or a number
less than 0 if the send has failed.

## Options Argument

The last argument is optional, and is only used with WebSockets. It
allows you to choose between sending binary or text data. Either of
these constants can be specified in this argument:

|                                                                                                              |                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------|
|  [Network Send Type Constant](../../../../GameMaker_Language/GML_Reference/Networking/network_send_raw)  |                       |
| Constant                                                                                                     | Description           |
|  network_send_binary                                                                                         | Send a binary message |
|  network_send_text                                                                                           | Send a text message   |

The APIs for some platforms only accept text messages when using
WebSockets (e.g. Twitch), so the network_send_text constant can be used
in such cases. If this argument is not specified, binary data is sent by
default.

#### Syntax:

``` gml
network_send_raw(socket, bufferid, size, [options]);
```

|          |                                                                                                              |                                                                                                               |
|----------|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                         | Description                                                                                                   |
| socket   |  [Network Socket ID](../../../../GameMaker_Language/GML_Reference/Networking/network_create_socket)      | The id of the socket to use.                                                                                  |
| bufferid |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                         | The id of the buffer to get the data from.                                                                    |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                          | The size (in bytes) of the data.                                                                              |
| options  |  [Network Send Type Constant](../../../../GameMaker_Language/GML_Reference/Networking/network_send_raw)  |  OPTIONAL Used for WebSockets to choose between text and binary data; if not specified, binary data is sent.  |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
buff = buffer_load("player_save.dat");
network_send_raw(sock, buff, buffer_get_size(buff));
```

The above information loads a previously saved buffer data into memory
and returns the buffer id to be stored in the variable "buff". This
complete buffer is then send as a raw data packet over the network using
the socket identified by the variable "sock".
