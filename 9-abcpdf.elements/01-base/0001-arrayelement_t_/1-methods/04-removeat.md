# RemoveAt Function

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

Removes the [Element](1086-element/default.md) at the specified index.

When an [Element](1086-element/default.md) is removed the items that follow the removed item, move up to occupy the vacated spot.
