---
title: "1-refatom"
css: "abcpdf-docs.css"
---

# RefAtom Constructor

Construct a RefAtom.

## Syntax

**[C#]**

```csharp
RefAtom()
RefAtom(IndirectObject value)
```

**[Visual Basic]**

```
Sub New()
Sub New(value As IndirectObject)
```

## Params

| Name | Description | 
| --- | --- |
| value | The initial IndirectObject that the Atom should point to. | 

## Notes

Create a RefAtom.

If an [IndirectObject](../../../6-abcpdf.objects/1-indirectobject/default.md) is not specified the default of the null object at entry zero will be used.

## Example

None.