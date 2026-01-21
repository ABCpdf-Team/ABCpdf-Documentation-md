---
title: "05-validate"
css: "abcpdf-docs.css"
---

# Validate Function

Validate this object and report any inconsistencies.

## Syntax

**[C#]**

```csharp
virtual void Validate(Validation validation)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function Validate(validation As Validation) As void`
			
## Params

| Name | Description | 
| --- | --- |
| validation | The Validation object which will receive validation results and progress. | 

## Notes

Validate this object and report any inconsistencies.

The validation of one object involves validating the properties of the object. Since.

the properties are often objects themselves, the process can be quite involved.

## Example

None.