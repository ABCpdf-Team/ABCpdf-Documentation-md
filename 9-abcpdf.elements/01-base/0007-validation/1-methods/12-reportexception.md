# ReportException Function

Called to report an Exception that was thrown during validation.

## Syntax

**[C#]**

```csharp
virtual void ReportException(Element element, Exception ex)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ReportException(element As Element, ex As Exception) As void`
			
## Params

| Name | Description | 
| --- | --- |
| element | The Element which was being processed. | 
| ex | The Exception which was thrown. | 

## Notes

Called to report an Exception that was thrown during validation.

In general you do not want the validation of one [Element](../../1086-element/default.md) to affect another.

So if an Exception is thrown during the validation of one [Element](../../1086-element/default.md), you want this to be reported, but then for validation to continue.

In the event that this happens, this function will be called.

## Example

None.