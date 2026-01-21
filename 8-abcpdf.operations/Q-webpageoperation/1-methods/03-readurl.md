# ReadUrl Function

Read a URL into a paged PDF document.

## Syntax

**[C#]**

```csharp
ReadUrl(string url)
```

<span class=language>[Visual Basic]</span>  

            `ReadUrl(url As String)`
			
## Params

| Name | Description | 
| --- | --- |
| url | The URL to read. | 

## Notes

Read a URL into a paged PDF document.

On return all [Doc](../2-properties/01-doc.md) properties are reset to default values.

This method works in a similar way to [Doc.AddImageUrl](/Manual/5-abcpdf/doc/1-methods/addimageurl.md) and so it is worth reading the notes for that function.

## Example

None.
            Also see example code in: [WebPageOperation Doc Property](../2-properties/01-doc.md).