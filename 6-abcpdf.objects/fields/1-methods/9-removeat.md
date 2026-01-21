---
title: "9-removeat"
css: "abcpdf-docs.css"
---

# RemoveAt Function

Removes an item at a specified position from the collection.

## Syntax

**[C#]**

```csharp
void RemoveAt(int index)
```

**[Visual Basic]**

`Sub RemoveAt(index As Integer)``may throw NotSupportedException()`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index of the item to remove. | 

## Notes

Removes an item from the collection.

All Fields collections are read only so calling this function will generate a NotSupportedException..

## Example

None.