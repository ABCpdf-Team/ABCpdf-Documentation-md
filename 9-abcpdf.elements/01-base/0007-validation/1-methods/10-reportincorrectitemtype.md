---
title: "10-reportincorrectitemtype"
css: "abcpdf-docs.css"
---

# ReportIncorrectItemType Function

Called to report an object which is of the wrong type.

## Syntax

**[C#]**

```csharp
virtual void ReportIncorrectItemType(string expectedType, string actualType, Atom atom)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ReportIncorrectItemType(expectedType As string, actualType As string, atom As Atom) As void`
			
## Params

| Name | Description | 
| --- | --- |
| expectedType | The expected type name. | 
| actualType | The actual type name. | 
| atom | The atom which was found. | 

## Notes

Called to report an object which is of the wrong type.

Some entries are required to specific types of object.

For example a Page Node has children which must be either other Page Nodes or Pages.

If an item like this is retrieved, and turns out to be a different type, this function will be called.

## Example

None.