---
title: "02-getenumerator"
css: "abcpdf-docs.css"
---

# GetEnumerator Function

Returns an enumerator that iterates through the [DictElement](../../0003-dictelement_t_/default.md).

## Syntax

**[C#]**

```csharp
virtual Enumerator GetEnumerator()
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function GetEnumerator() As Enumerator`
			
## Params

| Name | Description | 
| --- | --- |
| return | An enumerator for the collection. | 

## Notes

Returns an enumerator that iterates through the [DictElement](../../0003-dictelement_t_/default.md).

Get a KeyValuePair enumerator for the dictionary.

DictAtom.Enumerator is a value type that implements IEnumerator> and IDictionaryEnumerator.

## Example

None.