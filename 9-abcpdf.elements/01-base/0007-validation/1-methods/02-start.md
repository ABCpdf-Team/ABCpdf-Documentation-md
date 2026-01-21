# Start Function

Called at the point each [Element](../../1086-element/default.md) starts validation.

## Syntax

**[C#]**

```csharp
virtual bool Start(Element element)
virtual void Start(string entry)
virtual void Start(int index)
```

<span class=language>[Visual Basic]</span>  

```
Overridable Function Start(element As Element) As Boolean
Overridable Function Start(entry As string) As void
Overridable Function Start(index As int) As void
```

## Params

| Name | Description | 
| --- | --- |
| element | The element. | 
| entry | The new key or entry. | 
| index | The new index. | 

## Notes

Called at the point each [Element](../../1086-element/default.md) starts validation.

If the [Element](../../1086-element/default.md) has already been seen then this function should return false to indicate that it has already been validated.

If not then the function should return true to indicate that validation should go ahead.

Subclasses should keep track of elements that they have seen so as to avoid recursive loops.

## Example

None.