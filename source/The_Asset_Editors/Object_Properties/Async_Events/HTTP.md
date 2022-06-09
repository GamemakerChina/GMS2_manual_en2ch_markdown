# HTTP

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Async_HTTP.png)  
The HTTP Event is one that is triggered by the callback from one of the
[ http\_\*()
functions](../../../GameMaker_Language/GML_Reference/Asynchronous_Functions/HTTP/HTTP)
, like [ http_post_string()
](../../../GameMaker_Language/GML_Reference/Asynchronous_Functions/HTTP/http_post_string)
. It actually generates a [DS
Map](../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/DS_Maps)
that is exclusive to this event and is stored in the special variable
[async_load](../../../GameMaker_Language/GML_Overview/Variables/Builtin_Global_Variables/async_load)
(please see the individual functions for code examples that explain the
use of this event in further detail). This DS map has the following
general structure:

-   " id ": The id which was returned from the command. If you fire off
    a series of http\_ requests then you need to know which one you are
    getting the reply to, and so you would use this value to compare to
    the value you stored when you originally sent the request to find
    the right one.
-   " status ": Returns a value of less than 0 for an error, 0 for
    success and 1 if content is being downloaded.
-   " result ": The data received (string only), or the path to the file
    downloaded if you have used [ http_get_file()
    ](../../../GameMaker_Language/GML_Reference/Asynchronous_Functions/HTTP/http_get_file)
    . You may only get this key if the status is 0, but that is
    platform-dependent.
-   " url ": The complete URL you requested.
-   " http_status ": The raw http status code (if available). This
    returns the standard web status code for most browsers, eg: 304 for
    "Not Modified" or 204 for "No Content", etc...

The above shows what you get when you use the [ http_post_string()
](../../../GameMaker_Language/GML_Reference/Asynchronous_Functions/HTTP/http_post_string)
function, but each of the http\_ functions may return a slightly
different map, so please refer to the manual entry for each function to
find out the precise data that is returned for it. **NOTE** : As
async_load creates a DS map, these functions are particularly useful
when coupled with the [ json_encode()
](../../../GameMaker_Language/GML_Reference/File_Handling/Encoding_And_Hashing/json_encode)
and [ json_decode()
](../../../GameMaker_Language/GML_Reference/File_Handling/Encoding_And_Hashing/json_decode)
functions. There could also be additional data supplied by this map if
you have requested files for downloading. In this case, the "status"
will have a value of 1 and the DS map will hold these extra keys:

-   " contentLength ": This is the size of file that the web server has
    said you should expect to receive (may be -1 if the server does not
    return this data).
-   " sizeDownloaded ": The size of the data that has already been
    downloaded.

Note that the event will not be triggered for every single data packet
that is received, but will rather update at any time during the download
within the main game loop. Also note that currently this functionality
is only available for regular Windows target platforms.
