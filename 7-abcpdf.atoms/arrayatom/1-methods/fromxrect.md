# FromXRect Function

Create an ArrayAtom from a XRect representation

## Syntax

**[C#]**

```csharp
static ArrayAtom FromXRect( WebSupergoo.ABCpdf13.XRect value)
```

<span class=language>[Visual
            Basic]</span>  

            `Shared Function FromXRect(value As WebSupergoo.ABCpdf13.XRect) As ArrayAtom`
## Params

| Name | Description | 
| --- | --- |
| value | The XRect representing the value of the object. | 

## Notes

Create an ArrayAtom from a XRect representation.

The ArrayAtom will contain four [NumAtoms](../../numatom/default.md) corresponding to the horizontal and vertical elements of two diagonally opposite corners.

## Example

None.