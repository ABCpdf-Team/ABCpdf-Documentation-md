# FontEmbed Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether fonts should be embedded rather than referenced. | 

## Notes

This property determines whether fonts are embedded.

HTML rendering may require that fonts are added to the PDF document.

By default these fonts are - where possible - referenced. You can use this setting to ensure that fonts are embedded. This will increase output fidelity at a cost of processing time and output file size.

## Example

None.