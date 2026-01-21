# RichMediaAnnotation Function

Adds rich media to the current page of the doc.

## Syntax

**[C#]**

```csharp
RichMediaAnnotation(Doc doc, XRect rect, string filePathOrUrl, string mediaType)
```

<span class=language>[Visual Basic]</span>  

            `RichMediaAnnotation(doc As Doc, rect As XRect, filePathOrUrl As string, mediaType As string)`
			
## Params

| Name | Description | 
| --- | --- |
| doc | Doc | 
| rect | Annotation rectangle | 
| filePathOrUrl | Media file path or URL | 
| mediaType | Media type | 

## Notes

Adds rich media to the current page of the doc.

The media type can be one of:

- "Flash"
- "Video"
- "Sound"
- "3D"

Supported file formats are not defined by the PDF specification and thus will vary between viewers.

## Example

None.