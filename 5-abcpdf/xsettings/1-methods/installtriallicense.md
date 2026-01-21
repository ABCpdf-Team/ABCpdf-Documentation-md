---
title: "installtriallicense"
css: "abcpdf-docs.css"
---

# InstallTrialLicense Method

Install a trial license

## Syntax

**[C#]**

```csharp
bool InstallTrialLicense(string license)
```

<span class=language>[Visual Basic]</span>  
`Function InstallTrialLicense(license As String) As Boolean`
## Params

| Name | Description | 
| --- | --- |
| license | The license to install. | 
| return | True if a license is installed, otherwise false. | 

## Notes

Use this method to install a trial license. Call this method at application startup before any ABCpdf objects have been created. You only need to call this method once though calling it additional times will not cause problems.

Any license installed using this method will remain available to the current process (or application pool) until it unloads.

## Example

See [Manual Installation](../../../3-concepts/6-installation.md).