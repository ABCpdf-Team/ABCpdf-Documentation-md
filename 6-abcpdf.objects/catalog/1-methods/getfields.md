---
title: "getfields"
css: "abcpdf-docs.css"
---

# GetFields Function

Get all the eForm fields in the document.

## Syntax

**[C#]**

```csharp
IndirectObject[] GetFields()
```

**[Visual Basic]**

`Function GetFields() As IndirectObject()`
## Params

| Name | Description | 
| --- | --- |
| return | All the eForm fields in the document. | 

## Notes

This function scans the field tree and builds an array of all the fields in the document.

Most fields are [Annotations](../../annotation/default.md) which means they have a visible appearance on the page. All fields are [IndirectObjects](../../1-indirectobject/default.md).

## Example

None.