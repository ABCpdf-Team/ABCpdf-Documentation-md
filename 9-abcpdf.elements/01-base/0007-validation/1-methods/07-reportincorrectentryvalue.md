# ReportIncorrectEntryValue Function

Called to report an entry with an incorrect value.

## Syntax

**[C#]**

```csharp
virtual void ReportIncorrectEntryValue(string value)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ReportIncorrectEntryValue(value As string) As void`
			
## Params

| Name | Description | 
| --- | --- |
| value | The incorrect value. | 

## Notes

Called to report an entry with an incorrect value.

Many entries have values which are constrained.

For example some numbers may have a range between which they must fall.

Some numbers may be cardinal only. Names are often used to indicated enumerated options.

In the event that a value is incorrect this function will be called.

## Example

None.