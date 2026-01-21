# EntryLookup Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | This property represents the lookup table for the palette. | 

## Notes

This property represents the lookup table for the palette.

The lookup may be represented as a [StreamElement](../../../07-syntax/1028-streamelement/default.md) or (in PDF 1.2) a byte string.

The table shall contain a number of colors one higher than the [EntryHiVal](02-entryhival.md).

Each color shall contain a number of byes equal to the number of components in the [EntryBaseColorSpace](01-entrybasecolorspace.md).

Each byte represents an intensity of color from 0 to 255 - 0% to 100% respectively.

For definitive details see:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 156.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=164)

## Example

None.