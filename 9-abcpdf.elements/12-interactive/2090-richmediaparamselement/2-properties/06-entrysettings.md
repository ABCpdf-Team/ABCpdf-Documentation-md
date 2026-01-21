# EntrySettings Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | Represents the "Settings" entry of the richmediaparams dictionary object. | 

## Notes

Represents the "Settings" entry of the richmediaparams dictionary object.

It is defined as part of the PDF 1.0 specification.

This property may contain one of two different types:.

1) A string representing a PDF string object.

The PDF specification states that this item assumes a value of "undefined" if no value has been provided.

2) A [StreamElement](../../../07-syntax/1028-streamelement/default.md).

For definitive details see:.

[Adobe Supplement to the ISO 32000, BaseVersion: 1.7, ExtensionLevel: 3; Table: 9.51c, page 90.](http://www.adobe.com/content/dam/Adobe/en/devnet/acrobat/pdfs/adobe_supplement_iso32000.pdf#page=90)

## Example

None.