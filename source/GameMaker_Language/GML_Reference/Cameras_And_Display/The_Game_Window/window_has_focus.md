# window_has_focus

With this function you can poll the window (or tab) state and if it
loses focus the function will return false otherwise it will return true
. In most cases you can simply use the [ os_is_paused()
](../../OS_And_Compiler/os_is_paused) function to test this, but in
some very specific cases (for example games on Chrome Apps) that
function will not trigger, in which case you should use this function
instead. **NOTE** : This function is only valid for the HTML5, Windows,
and MacOS.

#### Syntax:

``` gml
window_has_focus();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !window_has_focus()
{
    PauseGame();
}
```

The above code will check to see if the game window is in focus or not,
and if the function returns false a function will be called.
