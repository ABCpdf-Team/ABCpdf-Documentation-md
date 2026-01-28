# Import Function

Imports a portion of an XPS document.

## Syntax

[C#]

```csharp
void Import(Doc doc, string path)
```

## Params

| **Name** | **Description** |
| --- | --- |
| doc | The target PDF document. |
| path | The file path to the XPS document. |

## Notes

Imports an XPS or OXPS Document. By default, the entire XPS document is imported.

An exception will be thrown if the operation is not possible. This may happen if the XPS document is corrupt.

You may notice that colors in the PDF files are slightly different. PDF handles alpha blending differently from other file formats. Refer to [SwfImportOperation.Import](5-swfimportoperation/1-methods/import.md) for notes about alpha blending.

Unless stated otherwise, a [ProcessedObject](1-operation/3-events/2-processedobject.md) event corresponding to each [ProcessingObject](1-operation/3-events/1-processingobject.md) event is generated with an object as follows:

Imported images are not compressed. You may wish to analyse and compress these [PixMap](6-abcpdf.objects/pixmap/default.md) objects by pre and post processing them during the [ProcessingObject](1-operation/3-events/1-processingobject.md) and [ProcessedObject](1-operation/3-events/2-processedobject.md) events.

## Example

Here we import the pages with odd page numbers of an XPS document up to page 8, 2 pages per sheet in landscape. The aspect ratio is preserved and a border is also drawn.

[C#]

```csharp
using var doc = new Doc();
var importOp = new MyImportOperation(doc);
importOp.Import("../mypics/AdvancedGraphicsExamples.xps");
doc.Save("xps.pdf");
```

![](../../../images/pdf/xps.pdf.png)
&nbsp;

