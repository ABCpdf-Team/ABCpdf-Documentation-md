---
title: "02-settarget"
css: "abcpdf-docs.css"
---

# SetTarget Function

Sets the page and type for the destination.

## Syntax

**[C#]**

```csharp
virtual void SetTarget(PageObjectElement page, DestinationType type)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function SetTarget(page As PageObjectElement, type As DestinationType) As void`			
## Params

| Name | Description | 
| --- | --- |
| page | The destination page. | 
| type | The type of destination. | 

## Notes

Sets the page and type for the destination.

As part of this process other destination parameters are set to defaults.

See [EntryType](../2-properties/02-entrytype.md) for details of the types that can be provided.

## Example

None.