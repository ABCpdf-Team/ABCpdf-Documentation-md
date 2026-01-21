---
title: "03-getresource"
css: "abcpdf-docs.css"
---

# GetResource Function

Gets a resource from the resources dictionary.

## Syntax

**[C#]**

```csharp
virtual AtomAndObject GetResource(IndirectObject owner, ResourceType type, string name)
virtual AtomAndObject GetResource(IndirectObject owner, Page page, ResourceType type, string name)
```

<span class=language>[Visual Basic]</span>  

```
Overridable Function GetResource(owner As IndirectObject, type As ResourceType, name As string) As AtomAndObject
Overridable Function GetResource(owner As IndirectObject, type As ResourceType, name As string) As AtomAndObject
```
			
## Params

| Name | Description | 
| --- | --- |
| owner | The owner of the stream - either a Page or Form XObject. | 
| page | The Page on which the owner is to be displayed. This may be null. | 
| type | The type of resource. For example this might be "Font". | 
| name | The name of the resource as referenced in the content stream. | 
| return | The resource. | 

## Notes

Gets a resource from the resources dictionary.

Resources are cached for fast lookup of repeated requests.

The ResourceType enumeration may take the following values:

- ExtGState - External graphics states.
- ColorSpace - Color space for graphics.
- Pattern - Pattern for filling areas.
- Shading - Shading type for filling areas.
- XObject - Encapsulated image in raster or vector form.
- Font - Font typeface for drawing text.
- ProcSet - Predefined procedure sets. This property is deprecated in the PDF specification.
- Properties - Marked content properties.

You do not have to specify a page and for almost all modern PDF documents it is unnecessary. However, while it strongly discourages it, the PDF specification allows Form XObjects to reference resources on the current Page rather than in the Form XObject itself. So for absolute correctness it is a good idea.

## Example

None.