# Start Function

## Syntax

[C#]

```csharp
virtual bool Start(<a href="../../1086-element/default.htm">Element</a> element)virtual void Start(string entry)virtual void Start(int index)
```

[Visual Basic]

```vb
Overridable Function Start(element As <a href="../../1086-element/default.htm">Element</a>) As BooleanOverridable Function Start(entry As string) As voidOverridable Function Start(index As int) As void
```

## Params

| **Name** | **Description** |
| --- | --- |
| element | The element. |
| entry | The new key or entry. |
| index | The new index. |

## Notes

Called at the point each [Element](1086-element/default.md) starts validation.

If the [Element](1086-element/default.md) has already been seen then this function should return false to indicate that it has already been validated.

If not then the function should return true to indicate that validation should go ahead.

Subclasses should keep track of elements that they have seen so as to avoid recursive loops.
