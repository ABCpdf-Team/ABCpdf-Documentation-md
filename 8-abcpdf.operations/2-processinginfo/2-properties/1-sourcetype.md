---
title: "1-sourcetype"
css: "abcpdf-docs.css"
---

# SourceType Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp ProcessingSourceType ``` [Visual Basic]`ProcessingSourceType` | See description. | Yes | Gets the type of the source object to be processed and the stage of operation. | 

## Notes

The ProcessingSourceType enumeration may take the following values:

- Unknown
- Document
- Page
- PageContent
- Image
- ImageMask
- MultiFrameImage
- ImageFrame
- Stream
- Path
- Text
- FormXObject
- Shading

The meaning of these source types depends on the operations.

## Example

None.