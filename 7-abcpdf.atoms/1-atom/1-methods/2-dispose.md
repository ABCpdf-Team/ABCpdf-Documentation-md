---
title: "2-dispose"
css: "abcpdf-docs.css"
---

# Dispose Function

Dispose of the object.

## Syntax

**[C#]**

```csharp
void Dispose()
protected void Dispose(bool disposing)
```

<span class=language>[Visual
            Basic]</span>  

```
Sub Dispose()
Protected Sub Dispose(disposing As Boolean)
```

## Params

| Name | Description | 
| --- | --- |
| none |  | 

## Notes

You can call this function to explicitly dispose of an object and reduce the garbage collection overhead.

This method follows the standard design pattern for objects implementing the IDisposable interface. The protected Dispose method can be overridden for sub-classes wishing to dispose of additional objects.

Do not attempt to use an object after calling Dispose.

## Example

None.