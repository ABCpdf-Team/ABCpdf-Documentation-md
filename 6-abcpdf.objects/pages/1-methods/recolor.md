# Recolor Function

Converts the pages from one color space to another.

## Syntax

**[C#]**

```csharp
void Recolor(ColorSpace space, bool convertAnnotations)
void Recolor(ColorSpace space, bool convertAnnotations, out PixMap[] recoloredPixMaps)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub Recolor(space As ColorSpace, convertAnnotations As Boolean)
Sub Recolor(space As ColorSpace, convertAnnotations As Boolean,  ByRef recoloredPixMaps As PixMap())
```
`may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| space | The destination color space. | 
| convertAnnotations | Whether to convert the color space of annotation appearance streams. | 
| recoloredPixMaps | All the PixMaps which were recolored as a result of the call. | 

## Notes

Converts the pages from one color space to another.

This method calls the [Page.Recolor](../../page/1-methods/recolor.md) method on all Page objects within this group of pages.

## Example