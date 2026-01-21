---
title: "setappearance"
css: "abcpdf-docs.css"
---

# SetAppearance Function

Set a particular appearance for the annotation.

## Syntax

**[C#]**

```csharp
virtual void SetAppearance(string state, string name, FormXObject form)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function SetAppearance(state As string, name As string, form As FormXObject) As void`
			
## Params

| Name | Description | 
| --- | --- |
| state | The state may be N, D, or R. These values represent the normal, down and rollover states respectively. | 
| name | The name for the state for choice fields which have names. This value may be null if this is not a choice field. | 
| form | The appearance. Pass null to remove the appearance. | 
| return | The appearance. | 

## Notes

Set a particular appearance for the annotation.

## Example

None.