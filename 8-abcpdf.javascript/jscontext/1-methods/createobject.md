---
title: "createobject"
css: "abcpdf-docs.css"
---

# CreateObject Method

Creates a JavaScript object.

## Syntax

**[C#]**

```csharp
JSValue CreateObject()
```

<span class=language>[Visual
            Basic]</span>  
`Function CreateObject() As JSValue``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| return | A new JavaScript object. | 

## Notes

The method creates a JavaScript object. It is much better than calling [ConvertToJS](converttojs.md) with an empty array of KeyValuePair.

## Example

None.