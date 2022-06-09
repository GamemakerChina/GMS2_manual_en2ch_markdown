# http_get_request_crossorigin

This function can be used to get the cross-origin type set for HTML5
games and will return a string (on all other platforms an empty string
"" will be returned).

#### Syntax:

``` gml
http_get_request_crossorigin();
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if string_lower(http_get_request_crossorigin()) != "use-credentials"
{
    http_set_request_crossorigin("use-credentials");
}
sprite_add("sprites/player_outfit_1.png", 0, false, false, 0, 0);
```

The above code will first check the currently set cross origin type and
if it is not "use-credentials" then it is set to "use-credentials" and
then a sprite is added from a file.
