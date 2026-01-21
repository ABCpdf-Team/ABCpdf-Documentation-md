# FromGray Function

Create an XColor from a grayscale value.

## Syntax

**[C#]**

```csharp
static XColor FromGray(int gray)
static XColor FromGray(double gray)
```

<span class=language>[Visual
            Basic]</span>  

```
Shared Function FromGray(gray As Integer) As XColor
Shared Function FromGray(gray As Double) As XColor
```

## Params

| Name | Description | 
| --- | --- |
| gray | The amount of black (0 to 255) | 
| return | The resulting XColor. | 

## Notes

Create an XColor from a grayscale value ranging between zero and 255.

The value represents the amount of black ink so zero indicates white and 255 indicates black.

## Example

None.