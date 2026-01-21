---
title: "detach"
css: "abcpdf-docs.css"
---

# Detach Function

Detaches a content stream from the page.

## Syntax

**[C#]**

```csharp
void Detach(StreamObject layer)
```

<span class=language>[Visual Basic]</span>  
`Sub Detach(layer As StreamObject)`
## Params

| Name | Description | 
| --- | --- |
| layer | The stream to detach from the page. | 

## Notes

Detaches a content stream from the page.

The layer is not deleted it is simply that any reference to it is removed from the page.

## Example

None.