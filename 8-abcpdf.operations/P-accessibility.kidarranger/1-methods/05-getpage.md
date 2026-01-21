# GetPage Function

Get the Page object for this particular structure element.

## Syntax

**[C#]**

```csharp
GetPage(this StructureElementElement element)
GetPage(this StructureElementElement element, Accessibility.Structure structure)
```

<span class=language>[Visual Basic]</span>  

```
GetPage(this StructureElementElement element)
GetPage(this StructureElementElement element, Accessibility.Structure structure)
```

## Params

| Name | Description | 
| --- | --- |
| return | The page. | 

## Notes

Get the Page object for this particular structure element.

In the event that there is no specified page the function will look up through the parent hierarchy to find one.

If still no page is found it will scan through the hierarchy assigning pages to all the elements and then return one.

In the unlikely event that no page can be found, it will return null.

## Example

None.