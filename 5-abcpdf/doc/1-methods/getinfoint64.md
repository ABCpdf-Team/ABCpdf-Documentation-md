---
title: "getinfoint64"
css: "abcpdf-docs.css"
---

# GetInfoInt64 Function

Gets numeric information about an object.

## Syntax

**[C#]**

```csharp
long GetInfoInt64(int id, string type)
```

<span class=language>[Visual Basic]</span>  
`Function GetInfoInt64(id As Integer, type As String) As Long`
## Params

| Name | Description | 
| --- | --- |
| id | The Object ID of the object to be queried. | 
| type | The type of information to be retrieved. | 
| return | The returned integer. | 

## Notes

This function behaves identically to the [GetInfo](getinfo.md) method but returns a 64-bit integer rather than a string. If the information cannot be obtained or is not numeric, the return value will be zero.

## Example

See the [GetInfo](getinfo.md) function.