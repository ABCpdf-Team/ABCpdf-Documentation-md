# Dispose Function

Dispose of the object.

## Syntax

[C#]

```csharp
void Dispose()void Dispose(out <a href="../../xreadoptions/default.htm">XReadOptions</a> outOptions, out Stream outStream)protected void Dispose(bool disposing)
```

[Visual Basic]

```vb
Sub Dispose()Sub Dispose(&lt;Out&gt; ByRef outOption As <a href="../../xreadoptions/default.htm">XReadOptions</a>, &lt;Out&gt; ByRef outStream As Stream)Protected Sub Dispose(disposing As Boolean)
```

## Params

| **Name** | **Description** |
| --- | --- |
| outOptions | The XReadOptions used to create the object. |
| outStream | The Stream used to create the object if NeedsStream is true. |

## Notes

You can call this function to explicitly dispose of an object and reduce the garbage collection overhead.

The overload without parameters disposes of the [XReadOptions](xreadoptions/default.md) and of the Stream.

The overload with output parameters returns the [XReadOptions](xreadoptions/default.md) and the Stream. The returned objects have not been disposed of.

This method follows the standard design pattern for objects implementing the IDisposable interface. The protected Dispose method can be overridden for sub-classes wishing to dispose of additional objects.

Do not attempt to use an object after calling Dispose.

## Example

None
