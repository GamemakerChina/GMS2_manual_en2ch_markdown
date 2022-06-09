# randomise

This function sets the seed to a random value. Should you need to keep a
consistent value over a number of runs of a game, you should be using [
random_set_seed() ](random_set_seed) . Please note, that when using
the random number functions in GameMaker the initial seed is always the
same, as this makes tracing errors and debugging far easier. Should you
wish to test with true random, you should call this function at the
start of your game. The function will return the new randomised seed
value (an unsigned 32bit integer).

#### Syntax:

``` gml
randomise(); // or randomize();
```

#### Returns:

``` gml
 Real

(unsigned 32 bit value)
```

#### Example:

``` gml
randomise();
```

The above code will randomise the seed.
