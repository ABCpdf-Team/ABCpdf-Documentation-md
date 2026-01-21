---
title: "3-add"
css: "abcpdf-docs.css"
---

# Add Function

Add an item to the end of the collection.

## Syntax

**[C#]**

```csharp
int Add(Field field)
```

**[Visual Basic]**

`Function Add(field As Field) As Integer``may throw NotSupportedException()`

## Params

| Name | Description | 
| --- | --- |
| field | The item to be added. | 

## Notes

This method adds an item to the collection.

All Fields collections are read only so calling this function will generate a NotSupportedException.

## Example

None.