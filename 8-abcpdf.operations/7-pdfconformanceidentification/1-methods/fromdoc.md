---
title: "fromdoc"
css: "abcpdf-docs.css"
---

# FromDoc Function

Gets the conformance identification from a document.

## Syntax

**[C#]**

```csharp
static PdfConformanceIdentification FromDoc(Doc doc, PdfConformance conformance)
```

<span class=language>[Visual Basic]</span>  
`Shared Function FromDoc(doc As Doc, conformance As PdfConformance) As PdfConformanceIdentification`
## Params

| Name | Description | 
| --- | --- |
| doc | The document. | 
| conformance | The conformance specification for which the identification is to be retrieved. | 
| return | The conformance identification. | 

## Notes

This method identifies the conformance a document is marked to satisfy.

It is possible that a document conforms to more than one specification (e.g. PDF/A-1 and PDF/X-1) so you need to indicate which specification you want to retrieve the identification for.

The conformance parameter can take the following values:

- Pdf – not valid.
- PdfA1b - PDF/A-1 specification.
- PdfA1a - PDF/A-1 specification (exactly the same as PdfA1b).
- PdfA2b - PDF/A-2 specification.
- PdfA2u - PDF/A-2 specification (exactly the same as PdfA2b).
- PdfA2a - PDF/A-2 specification (exactly the same as PdfA2b).
- PdfUA1 - PDF/UA-1 specification.

## Example

None.