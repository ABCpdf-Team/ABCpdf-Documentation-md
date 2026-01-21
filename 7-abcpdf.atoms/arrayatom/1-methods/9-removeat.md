# RemoveAt Function

Removes an Atom at a specified position from the array.

## Syntax

**[C#]**

```csharp
void RemoveAt(int index)
```

**[Visual Basic]**

`Sub RemoveAt(index As Integer)``may throw ArgumentOutOfRangeException()`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index of the item to remove. | 

## Notes

If the index is not valid then an ArgumentOutOfRangeException will be thrown.

When an Atom is removed the elements that follow the removed element move up to occupy the vacated spot.

## Example

None.