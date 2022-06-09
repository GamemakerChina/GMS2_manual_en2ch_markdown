# url_open

This will open the specified URL on the browser of the chosen target
device, or, if you are using the HTML5 module, in the currently open
browser. NOTE Antivirus software installed on the player's device may
cause the URL to not open, so keep this in mind when using this
function.

#### Syntax:

``` gml
url_open(url);
```

|          |                                                                        |                                       |
|----------|------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                   | Description                           |
| url      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The URL (website address) to link to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
url_open("http://yoyogames.com");
```

This would open the YoYo Games homepage in the current window.
