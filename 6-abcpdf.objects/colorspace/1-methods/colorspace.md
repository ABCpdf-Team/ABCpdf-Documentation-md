# ColorSpace Constructor

Construct a ColorSpace.

## Syntax

**[C#]**

```csharp
ColorSpace(ObjectSoup soup)
ColorSpace(ObjectSoup soup, ColorSpaceType space)
```

**[Visual Basic]**

```
Sub New(soup As ObjectSoup)
Sub New(soup As ObjectSoup, space As ColorSpaceType)
```

## Params

| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created StreamObject. | 
| space | The type of color space required. | 

## Notes

Create a ColorSpace.

If a color space is not specified the default of DeviceRGB will be used.

## Example

See the [PixMap.Recolor](../../pixmap/1-methods/recolor.md) function.