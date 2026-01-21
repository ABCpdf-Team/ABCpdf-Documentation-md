---
title: "6-fromnums"
css: "abcpdf-docs.css"
---

# FromNums Function

Create an XRect from an array or list of four numbers.

## Syntax

**[C#]**

```csharp
static XRect FromNums(double[] array)
static XRect FromNums(IList list)
```

<span class=language>[Visual Basic]</span>  

```
Shared Function FromNums(array As Double()) As XRect
Shared Function FromNums(list As IList(Of Double)) As XRect
```

## Params

| Name | Description | 
| --- | --- |
| array | An array containing four doubles. | 
| list | An IList containing four doubles. | 
| return | The newly created XRect object. | 

## Notes

Create an XRect from an array or list of four numbers.

Such arrays typically contain lower left x and y coordinates followed by upper right x and y.

However this is a convention and any two diagonally opposite points are acceptable.

If the array is null or does not contain four items then the return will be null.

## Example

None.