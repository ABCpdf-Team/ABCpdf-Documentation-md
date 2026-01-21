# ContentStreamScanner Function

Create a new [ContentStreamScanner](../default.md).

## Syntax

**[C#]**

```csharp
ContentStreamScanner()
ContentStreamScanner(ContentStreamScanner sibling)
```

<span class=language>[Visual Basic]</span>  

```
ContentStreamScanner()
ContentStreamScanner(sibling As ContentStreamScanner)
```

## Params

| Name | Description | 
| --- | --- |
| sibling | A scanner which contains cached data. | 

## Notes

Create a new [ContentStreamScanner](../default.md).

A [ContentStreamScanner](../default.md) will cache useful resources as they are needed. If you are creating multiple [ContentStreamScanners](../default.md) for the same document you can share this cache to increase efficiency.

To share cached data in this way pass in a sibling scanner previously used to scan a content stream in the same doc.

## Example

None.