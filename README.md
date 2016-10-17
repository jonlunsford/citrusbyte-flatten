# Citrusbyte

This library contains custom Citrusbyte implementations of native functions,
For fun and profit.

All unit tests are in the form of doctests.

## Citrusbyte.flatten/1

Flattens multi dimensional arrays.
An array consisting of other nested arrays
will be recursively combined to form a single
array. The end 'tail' of the array will be added
to the end of the resulting array, First In First Out.

```
## Examples
    iex> Citrusbyte.flatten([])
    []

    iex> Citrusbyte.flatten([1])
    [1]

    iex> Citrusbyte.flatten([[1,2,[3]],4])
    [1,2,3,4]

    iex> Citrusbyte.flatten([[1,2,[]],4])
    [1,2,4]

    iex> Citrusbyte.flatten([[[1],[2, [3]],[4]],[5]])
    [1,2,3,4,5]
```
