# random_set_seed

To generate a random number GameMaker starts with a random seed number.
With this function you can set that seed to a known value and so "force"
the outcome of all random events afterwards to be the same every time
the program is run. For example, this function can be used in
conjunction with [ random_get_seed() ](random_get_seed) to create
procedurally generated content and save the results without having huge
savegames (you save the seed only, no need for anything else). Should
you need truly random results for everything, you should be using the [
randomise() ](randomise) function. NOTE While this seed will give
consistent results on each target platform, results may vary between
platforms due to the different way each target works.

#### Syntax:

``` gml
random_set_seed(val);
```

|          |                                                                         |                  |
|----------|-------------------------------------------------------------------------|------------------|
| Argument | Type                                                                    | Description      |
| val      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The seed to set. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if debug
{
    random_set_seed(1);
}
```

The above code sets the random seed to 1 only if the variable "debug" is
true.
