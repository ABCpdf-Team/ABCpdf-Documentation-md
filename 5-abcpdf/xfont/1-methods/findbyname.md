---
title: "findbyname"
css: "abcpdf-docs.css"
---

# FindByName Function

Find all the fonts with a given name.

## Syntax

**[C#]** ```csharp static XFont[] FindByName(string name) ``` [Visual Basic] `Shared Function FindByName(name As String) As XFont()`

## Params

| Name | Description | 
| --- | --- |
| name | The name of the font. | 
| return | The set of matching fonts. | 

## Notes

This function finds all the fonts with a given name.

Note that each font may contain many different names. Some names are more unique than others. So it is good to be as specific as possible when searching by name.

## Example

None.