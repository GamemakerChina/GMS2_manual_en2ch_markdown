# HTTP

This section lists all the different Asynchronous HTTP functions
available in GameMaker . These functions will generate an [Asynchronous
HTTP
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/HTTP)
in all instances that have it:

-   [http_request](http_request)
-   [http_get](http_get)
-   [http_get_file](http_get_file)
-   [http_post_string](http_post_string)

Please note that the above http\_\* functions may not function as
expected due to **cross domain security** issues. This means that
requests to your server or attempts to load resources from across
domains are blocked and may appear to return blank results or 404
errors. One of the ways you can get around this is to have some server
side PHP which allows certain domains to access your server (this is
also a way to protect your resources and block servers that are not
included in the PHP allow list). The following is an example of PHP code
you can use for this:

``` gml
$http_origin = $_SERVER['HTTP_ORIGIN'];
if ($http_origin == "http://127.0.0.1:51268")
{
    header("Access-Control-Allow-Origin: *");
}
```

For image load requests where determining or setting their cross-origin
type is important, the following functions exist:

-   [http_get_request_crossorigin](http_get_request_crossorigin)
-   [http_set_request_crossorigin](http_set_request_crossorigin)

In most cases these functions should not need to be used, but if the
game is stored on a secured server - where certain assets may require
basic authentication to be accessed and are generating security errors
when loading - setting the cross-origin type for image requests to
"use-credentials" may be necessary (as opposed to the default
"anonymous" setting).
