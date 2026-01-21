---
title: "01-autodetectfactory"
css: "abcpdf-docs.css"
---

# AutodetectFactory Function

Autodetect Factory.

## Syntax

**[C#]**

```csharp
static Element AutodetectFactory(Atom atom, IndirectObject host, object reference)
```

<span class=language>[Visual Basic]</span>  

            `Shared Function AutodetectFactory(atom As Atom, host As IndirectObject, reference As object) As Element`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The atom from which the Element should be created. | 
| host | The host object. This can be any IndirectObject in the document but it is useful to specify one with which the atom is closely associated. | 
| reference | A reference which may be used to pass context. | 
| return | An Element or Element subclass. | 

## Notes

Autodetect Factory.

This is used for the creation of specific types of [Element](../../1086-element/default.md) based on the content of the Atom.

Many Atoms have specific Type or Subtype fields which are used to indicate the precise variant of [Element](../../1086-element/default.md).

If these are present, which in many cases they are, then a sensible choice can be made as to the type of [Element](../../1086-element/default.md) to create.

Even when these are not present sometimes it is possible to detect the type from specific combinations of entries found in the Atom.

However not all specializations can be auto-detected as not all require this type of identification element.

If this is the case then the return value will be a generic [Element](../../1086-element/default.md).

## Example

None.