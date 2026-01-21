---
title: "08-reportmissingrequiredentry"
css: "abcpdf-docs.css"
---

# ReportMissingRequiredEntry Function

Called to report a missing required entry.

## Syntax

**[C#]**

```csharp
virtual void ReportMissingRequiredEntry()
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ReportMissingRequiredEntry() As void`
			
## Params

| Name | Description | 
| --- | --- |
| none |  | 

## Notes

Called to report a missing required entry.

Some entries are required to be present.

In the event that the entry is not provided, this function will be called.

## Example

None.