---
title: "1-renderoperation"
css: "abcpdf-docs.css"
---

# RenderOperation Constructor

RenderOperation Constructor.

## Syntax

**[C#]**

```csharp
RenderOperation(Doc doc)
```

<span class=language>[Visual
            Basic]</span>  
`Sub New(doc As Doc)`
## Params

| Name | Description | 
| --- | --- |
| doc | The PDF Document | 

## Notes

Create a RenderOperation to allow rendering of multiple pages from different threads.

You can use Doc.Rendering to set rendering options before creating a RenderOperation. When a RenderOperation is created, relevant doc properties are copied, so modifying properties of Doc.Rendering after creating the operation does not affect the RenderOperation. Likewise, setting the current page to another page after creating the operation has no effect.

## Example

See the [Save](save.md) method.