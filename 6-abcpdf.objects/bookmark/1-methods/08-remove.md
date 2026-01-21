---
title: "08-remove"
css: "abcpdf-docs.css"
---

# Remove Function

Removes a Bookmark from the list.

## Syntax

**[C#]**

```csharp
bool Remove(Bookmark value)
```

<span class=language>[Visual
            Basic]</span>  
`Function Remove(value As Bookmark) As Boolean`
## Params

| Name | Description | 
| --- | --- |
| value | The Bookmark to be removed. | 
| return | True if the Bookmark is removed, otherwise false. | 

## Notes

When a Bookmark is removed the elements that follow the removed element move up to occupy the vacated spot.

## Example

None.