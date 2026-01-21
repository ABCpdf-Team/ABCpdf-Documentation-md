---
title: "makefieldintogroup"
css: "abcpdf-docs.css"
---

# MakeFieldIntoGroup Function

Make duplicate fields into synchronized groups.

## Syntax

**[C#]**

```csharp
bool MakeFieldIntoGroup(Field inField)
```

<span class=language>[Visual Basic]</span>  

            `Function MakeFieldIntoGroup(inField As Field) As Boolean`
			
## Params

| Name | Description | 
| --- | --- |
| inField | The field to operate on | 

## Notes

Make duplicate fields into synchronized groups.

Scans through sibling fields looking for duplicate names.

Any duplicates are put together in a field group so that they will synchronize.

## Example

See the Annotations example project.
              None.