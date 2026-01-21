# AddAnnotations Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp XpsImportOperation.AnnotationFlags ``` [Visual Basic]`XpsImportOperation.AnnotationFlags` | None | No | The types of annotations to be added. | 

## Notes

This property specifies the types of annotations to be added for hyperlinks in the XPS file.

It can take a combination of the following values:

- None — This is the default value. No annotation is added.
- InternalLink — Link annotations that point to pages in the same document are added.
- ExternalLink — Link annotations that link to external resources (e.g. URLs) are added.

## Example

None.