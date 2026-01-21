# Clear Function

Clears the image.

## Syntax

**[C#]**

```csharp
void Clear()
void Clear(out XReadOptions outOptions, out Stream outStream)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub Clear()
Sub Clear( ByRef outOption As XReadOptions,  ByRef outStream As Stream)
```

## Params

| Name | Description | 
| --- | --- |
| outOptions | The XReadOptions used to create the object. | 
| outStream | The Stream used to create the object if NeedsStream is true. | 

## Notes

Use this method to release resources and return the image to a just-created state.

The overload without parameters disposes of the [XReadOptions](../../xreadoptions/default.md) and of the Stream.

The overload with output parameters returns the [XReadOptions](../../xreadoptions/default.md) and the Stream. The returned objects have not been disposed of.

## Example