# AddResource Function

Add a particular type of resource to the page

## Syntax

[C#]

```csharp
string AddResource(<a href="../../1-indirectobject/default.htm">IndirectObject</a> resource, string type, string name)
```

[Visual Basic]

```vb
Function AddResource(resource As <a href="../../1-indirectobject/default.htm">IndirectObject</a>, type As String, name As String) As String
```

## Params

| **Name** | **Description** |
| --- | --- |
| resource | The resource to be added. |
| type | The type of resource. |
| name | The format of the name that should be used. |

## Notes

Add a particular type of resource to the page.

Pages may contain default resources usable by the page content stream. The most common resource types are "Font", "XObject" and "ColorSpace". For further details see the PDF Specification.

This method allows you to add new resources to the page. You may supply your own name for the resource but if the name is already in use, it may need to be modified. For this reason the function returns the value which was actually used for the addition.

## Example

None
