# EntryIntent Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IList ``` [Visual Basic] `IList` | null | No | Represents the "Intent" entry of the optional content group dictionary object. | 

## Notes

Represents the "Intent" entry of the optional content group dictionary object.

It is an optional entry defined as part of the PDF 1.0 specification.

It contains an array which contains strings, representing PDF name objects.

The PDF specification states that items in this array assume a value of "View" if no value has been provided.

Items in this array may take one of the following valid values:.

- View
- Design

.If you read the specification you will see that an array of one string may be represented as a single string rather than an array. However we always present this property as an array to simplify the interface. It is only if you add or remove items in the array, that the underlying representation will be changed.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 98, page 222.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=230)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 96, page 274.](https://www.iso.org/standard/63534.md)

## Example

None.