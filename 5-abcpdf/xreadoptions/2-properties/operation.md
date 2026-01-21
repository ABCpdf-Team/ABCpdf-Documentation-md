---
title: "operation"
css: "abcpdf-docs.css"
---

# Operation Property

| Type | Default | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp Operation ``` [Visual Basic]`Operation` | null | No | Gets or sets the Operation to use. | 

## Notes

This property is used by modules for which a suitable derived class of [Operation](../../../8-abcpdf.operations/1-operation/default.md) exists. If it is null, those modules create a temporary [Operation](../../../8-abcpdf.operations/1-operation/default.md) with default behaviours.

| ReadModule | Operation | Description | 
| --- | --- | --- |
| SwfVector | SwfImportOperation | If this property is null, the temporary SwfImportOperation has its Timeout set to Timeout and sets ProcessingObjectEventArgs.Info.FrameNumber to Frame once. | 
| Xps | XpsImportOperation | If this property is null, the temporary XpsImportOperation compresses the GraphicLayer's of the pages. | 
| XpsAny | XpsImportOperation | If this property is null, the temporary XpsImportOperation compresses the GraphicLayer's of the pages. | 

## Example

None.