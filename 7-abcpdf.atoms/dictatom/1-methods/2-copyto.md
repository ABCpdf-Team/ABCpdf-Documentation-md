# CopyTo Function

Copies the Atoms into an array.

## Syntax

**[C#]**

```csharp
void CopyTo(Atom[] array, int index)
void CopyTo(KeyValuePairAtom>[] array, int index)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub CopyTo(array As Atom(), index As Integer)
Sub CopyTo(array As KeyValuePair(Of String, Atom)(), index As Integer)
```

## Params

| Name | Description | 
| --- | --- |
| array | The array that is the destination for the elements. | 
| index | The zero-based index in array at which copying begins. | 

## Notes

Copies the elements of the dictionary to an array starting at a particular array index.

The array must be one-dimensional and have zero-based indexing.

The implementation of ICollection.CopyTo copies KeyValuePair values to the array if the element type of the array is compatible. Otherwise, it copies DictionaryEntry values to the array.

## Example

None.