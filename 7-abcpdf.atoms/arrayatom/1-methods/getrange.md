# GetRange Function

Creates a shallow copy of a range of elements in the source array

## Syntax

**[C#]**

```csharp
ArrayAtom GetRange(int index, int count)
```

<span class=language>[Visual
            Basic]</span>  

            `Function GetRange(index As Integer, count As Integer) As ArrayAtom``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index specifying the first element. | 
| count | The number of elements to be selected. | 

## Notes

Creates a shallow copy of a range of elements in the source array.

If the index is equal to the [Count](../2-properties/count.md) then the elements are added to the end of the array. If the index or count is invalid then an exception will be raised.

## Example

None.