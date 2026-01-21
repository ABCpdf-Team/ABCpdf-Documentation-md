---
title: "8-remove"
css: "abcpdf-docs.css"
---

# Remove Function

Removes an item from the collection.

## Syntax

**[C#]**

```csharp
bool Remove(Field value)
```

**[Visual Basic]**

`Function Remove(value As Field) As Boolean``may throw NotSupportedException()`

## Params

| Name | Description | 
| --- | --- |
| value | The item to be removed. | 
| return | True if the item is removed, otherwise false. | 

## Notes

Removes an item from the collection.

All Fields collections are read only so calling this function will generate a NotSupportedException.

## Example

None.