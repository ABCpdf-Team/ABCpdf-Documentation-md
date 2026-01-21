---
title: "getvaluebool"
css: "abcpdf-docs.css"
---

# GetValueBool Method

Gets the Boolean value of this value converted to Boolean value using the standard JavaScript conversion.

## Syntax

**[C#]**

```csharp
bool GetValueBool()
```

<span class=language>[Visual
            Basic]</span>  
`Function GetValueBool() As Boolean``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| return | The Boolean value of the converted value. | 

## Notes

The method is the chain of [ToJSBoolean](tojsboolean.md) and [GetBooleanBool](getbooleanbool.md) without intermediate object creation.

## Example

None.