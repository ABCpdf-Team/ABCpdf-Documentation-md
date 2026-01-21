---
title: "getappearance"
css: "abcpdf-docs.css"
---

# GetAppearance Function

Get a particular appearance from the annotation.

## Syntax

**[C#]**

```csharp
virtual FormXObject GetAppearance(string state, string name)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function GetAppearance(state As string, name As string) As FormXObject`
			
## Params

| Name | Description | 
| --- | --- |
| state | The state may be N, D, or R. These values represent the normal, down and rollover states respectively. | 
| name | The name for the state for choice fields which have names. This value may be null if this is not a choice field. | 
| return | The appearance. | 

## Notes

Get a particular appearance from the annotation.

## Example

None.