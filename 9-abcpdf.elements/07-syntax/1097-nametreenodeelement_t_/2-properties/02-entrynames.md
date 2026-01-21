# EntryNames Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp ArrayElementElement> ``` [Visual Basic] `ArrayElementElement>` | null | No | This property represents the "Names" entry of the name tree node dictionary object. | 

## Notes

This property represents the "Names" entry of the name tree node dictionary object.

It is defined as part of the PDF 1.0 specification.

An Array containing alternate keys and values. For this reason the number of items in they array is always a multiple of two.

So to find the 10th key and value you would use a zero based index of 20 and 21 respectively.

The pairs in this array should be sorted in ascending order by key value.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 36, page 89.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=97)

## Example

None.