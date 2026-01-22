# RemoveAt Function

Removes the item at the specified index.

## Syntax

[C#]

```csharp
virtual void RemoveAt(int index)
```

[Visual Basic]

```vb
Overridable Function RemoveAt(index As int) As void
```

## Params

| **Name** | **Description** |
| --- | --- |
| index | The zero-based index of the item to remove. |

## Notes

Removes the item at the specified index.

When an item is removed the items that follow the removed item, move up to occupy the vacated spot.
