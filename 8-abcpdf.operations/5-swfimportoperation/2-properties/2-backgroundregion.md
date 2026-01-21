---
title: "2-backgroundregion"
css: "abcpdf-docs.css"
---

# BackgroundRegion&nbsp;Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp XRect ``` [Visual Basic]`XRect` | null | No | Gets or sets the backgound rectangle. | 

## Notes

The background region (in twips) is where the frame background is drawn. Set this property to change the extent or location of the background. The background region is set to the frame bounds/stage size if [ResetRegions](4-resetregions.md) is true. If it is null (and not set to non-null because of [ResetRegions](4-resetregions.md)), no background is drawn.

## Example

See the [Import](../1-methods/import.md) method.

Also see example code in: [SwfImportOperation Import Function](../1-methods/import.md).