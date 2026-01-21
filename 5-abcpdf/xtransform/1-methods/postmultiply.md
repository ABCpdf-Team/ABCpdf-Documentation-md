---
title: "postmultiply"
css: "abcpdf-docs.css"
---

# PostMultiply Function

Post-multiplies this transformation matrix by the supplied transform.

## Syntax

**[C#]**

```csharp
void PostMultiply(XTransform transform)
```

<span class=language>[Visual
            Basic]</span>  

            `Sub PostMultiply(transform as XTransform)`
## Params

| Name | Description | 
| --- | --- |
| transform | The transform to combine with this one. | 

## Notes

Post-multiplies this transformation matrix by the supplied transform.

The final result is contained in this transform.

See also the [PreMutiply](premultiply.md) function.

## Example

None.