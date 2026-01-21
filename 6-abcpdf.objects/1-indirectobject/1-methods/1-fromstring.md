---
title: "1-fromstring"
css: "abcpdf-docs.css"
---

# FromString Function

Construct an appropriate type of IndirectObject given a string value.

## Syntax

**[C#]**

```csharp
static IndirectObject FromString(string value)
```

**[Visual Basic]**

`Shared Function FromString(value As String) As IndirectObject`
## Params

| Name | Description | 
| --- | --- |
| value | The string representing the value of the object. | 
| return | The resulting IndirectObject. | 

## Notes

The text you pass this function must be in native PDF format. This means that unusual characters in text strings must be appropriately escaped.

For full details of the way that PDF objects are represented you should see the Adobe PDF Specification.

## Example

None.