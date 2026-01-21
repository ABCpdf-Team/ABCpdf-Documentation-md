---
title: "11-reportincorrectnumberofentries"
css: "abcpdf-docs.css"
---

# ReportIncorrectNumberOfEntries Function

Called to report an array with an incorrect number of entries.

## Syntax

**[C#]**

```csharp
virtual void ReportIncorrectNumberOfEntries(int expected, int found)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ReportIncorrectNumberOfEntries(expected As int, found As int) As void`
			
## Params

| Name | Description | 
| --- | --- |
| expected | The value which was expected. | 
| found | The value which was found. | 

## Notes

Called to report an array with an incorrect number of entries.

Some arrays have a set number of items.

For example a value range may be represented as an array with two elements indicating higher and lower bounds.

In the event that the number of entries is incorrect, this function will be called.

## Example

None.