# log2

This function basically asks "how many 2's do you need to multiply to
get n?". A common example of use in programming would be to calculate
the number of bits that are needed to represent a number. To do this we
calculate the log2(x) of the number, round it down and add 1 - for
example log2(100) returns 6.643856, which rounded down is 6, to which we
add one and it gives us 7. So we need 7 bits to represent 100. It can
also be used for describing exponential growth or decay, and is often
called a *binary logarithm* .

#### Syntax:

``` gml
log2(n);
```

|          |                                                                         |                  |
|----------|-------------------------------------------------------------------------|------------------|
| Argument | Type                                                                    | Description      |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The input value. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
colourbits = floor(log2(colour)) - 1;
```

The above code stores the number of bits needed to represent the value
stored in the variable "colour".
