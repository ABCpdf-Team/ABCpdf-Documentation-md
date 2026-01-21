---
title: "9-getenumerator"
css: "abcpdf-docs.css"
---

# GetEnumerator Function

Get an enumerator for the dictionary.

## Syntax

**[C#]**

```csharp
DictAtom.Enumerator GetEnumerator()
```

**[Visual Basic]**

`Function GetEnumerator() As DictAtom.Enumerator`
## Params

| Name | Description | 
| --- | --- |
| return | The enumerator for the dictionary. | 

## Notes

Get an KeyValuePair enumerator for the dictionary.

DictAtom.Enumerator is a value type that implements IEnumerator> and IDictionaryEnumerator.

## Example

None.