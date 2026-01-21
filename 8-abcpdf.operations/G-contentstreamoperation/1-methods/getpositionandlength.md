---
title: "getpositionandlength"
css: "abcpdf-docs.css"
---

# GetPositionAndLength Function

Gets the position and length of an operator and the parameters that it takes.

## Syntax

**[C#]**

```csharp
Tuple GetPositionAndLength(IndirectObject owner, ArrayAtom array, int index)
```

<span class=language>[Visual Basic]</span>  

            `Sub GetPositionAndLength(owner As IndirectObject, array As ArrayAtom, index As int) As Tuple`
			
## Params

| Name | Description | 
| --- | --- |
| owner | The owner of the operator. | 
| array | The content stream ArrayAtom. | 
| index | The index of the operator within the array. | 
| return | The position and length within the data. | 

## Notes

Gets the position and length of an operator and the parameters that it takes.

The item in the array at the index provided must be an OpAtom or an exception will be raised.

The position returned is relative to the complete content stream sequence.

To convert this to an offset within a particular stream you can pass the relevant.

offset to the GetStreamAndOffset function.

## Example

None.