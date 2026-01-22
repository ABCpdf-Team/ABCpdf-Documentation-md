# Remove Function

## Syntax

[C#]

```csharp
virtual bool Remove(T value)
```

[Visual Basic]

```vb
Overridable Function Remove(value As T) As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| value | The Element to remove. |
| return | True if the Element is removed, otherwise false. |

## Notes

Removes an [Element](1086-element/default.md) from the array.

When an [Element](1086-element/default.md) is removed, the items that follow the removed item move up to occupy the vacated spot.
