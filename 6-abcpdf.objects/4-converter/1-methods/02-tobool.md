---
title: "02-tobool"
css: "abcpdf-docs.css"
---

# ToBool Function

Attempts to get a boolean from the specified entry in a DictAtom or ArrayAtom resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual bool? ToBool(Atom atom, int index)
virtual bool? ToBool(Atom atom, string key)
virtual bool? ToBool(Atom atom)
```

<span class=language>[Visual Basic]</span>  

```
Overridable Function ToBool(atom As Atom, index As int) As Boolean?
Overridable Function ToBool(atom As Atom, key As string) As Boolean?
Overridable Function ToBool(atom As Atom) As Boolean?
```

## Params

| Name | Description | 
| --- | --- |
| atom | The DictAtom or ArrayAtom from which to obtain the value. | 
| index | The zero based index from which the value should be obtained. | 
| key | The key identifying the entry to be obtained. | 
| return | The value. | 

## Notes

Attempts to get a boolean from the specified atom resolving any references as necessary.

If the simple overload is used then the atom provided must resolve to a value of the correct type. If not then the return value will be null.

If a key is provided then the atom must resolve to a DictAtom and the entry in the DictAtom must resolve to a value of the correct type. If this is not the case or the key is null, then the return value will be null.

If an index is provided then the atom must resolve to an ArrayAtom and the indexed entry in the ArrayAtom must resolve to a value of the correct type. If this is not the case or if the index is not available, then the return value will be null.

## Example

None.