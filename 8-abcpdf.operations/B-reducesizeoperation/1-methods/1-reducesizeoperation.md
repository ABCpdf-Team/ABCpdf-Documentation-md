---
title: "1-reducesizeoperation"
css: "abcpdf-docs.css"
---

# ReduceSizeOperation Constructor

ReduceSizeOperation Constructor.

## Syntax

**[C#]**

```csharp
ReduceSizeOperation(Doc doc)
```

<span class=language>[Visual
            Basic]</span>  
`Sub New(doc As Doc)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| doc | The PDF Document | 

## Notes

Create a ReduceSizeOperation to compact and compress a PDF document. If the doc is null then an exception will be raised.

## Example

See the [Compact](compact.md) function.