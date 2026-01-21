# SetData Function

Set the raw binary content of the stream.

## Syntax

**[C#]**

```csharp
override void SetData(byte[] value)
```

<span class=language>[Visual
            Basic]</span>  
`Overrides Sub SetData(value() As Byte)``may throw Exception()`

## Params

| Name | Description | 
| --- | --- |
| value | The raw binary content of the stream. | 

## Notes

Set the raw binary content of the stream.

This function overrides the [StreamObject.SetData](../../streamobject/1-methods/setdata.md) function.

If the StreamObject currently contains compressed data or if the content provided is not a valid ICC profile then an exception will be thrown.

## Example

None.