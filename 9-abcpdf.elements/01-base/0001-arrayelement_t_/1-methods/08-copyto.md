# CopyTo Function

## Syntax

[C#]

```csharp
virtual void CopyTo(T[] array, int index)
```

[Visual Basic]

```vb
Overridable Function CopyTo(array() As T, index As int) As void
```

## Params

| **Name** | **Description** |
| --- | --- |
| array | The array that is the destination for the elements. |
| index | The zero-based index at which copying begins. |

## Notes

Copies the [Elements](1086-element/default.md) into an array.

Copies the elements of the collection to an array starting at a particular index.
