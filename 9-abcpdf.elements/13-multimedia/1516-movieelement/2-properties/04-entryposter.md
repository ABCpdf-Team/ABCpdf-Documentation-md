# EntryPoster Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "Poster" entry of the movie dictionary object. | 

## Notes

Represents the "Poster" entry of the movie dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A bool representing a PDF boolean object.

The PDF specification states that this item assumes a value of false if no value has been provided.

2) An [ImageXObjectElement](../../../08-graphics/1214-imagexobjectelement/default.md).

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 295, page 508.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=516)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 306, page 635.](https://www.iso.org/standard/63534.md)

## Example

None.