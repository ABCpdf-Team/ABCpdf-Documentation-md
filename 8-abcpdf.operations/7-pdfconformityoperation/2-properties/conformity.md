# Conformity Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp PdfConformity ``` [Visual Basic]`PdfConformity` | None | No | The PDF conformity. | 

## Notes

This property specifies the conformity operations to perform. They provides more precise specifications than [Conformance](conformance.md).

It can take a combination of the following values:

- None – no operation.
- NoJavaScriptAction – removes JavaScript actions. (included in PDF/A conformance.)
- NoDocMetadataWithUnknownNamespace – removes document metadata with unknown XML namespaces. (included in PDF/A conformance.)

## Example

None.