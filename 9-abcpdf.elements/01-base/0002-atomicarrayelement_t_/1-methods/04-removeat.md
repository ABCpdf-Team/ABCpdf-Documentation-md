---
title: "04-removeat"
css: "abcpdf-docs.css"
---

# RemoveAt Function

Removes the item at the specified index.

## Syntax

**[C#]**

```csharp
virtual void RemoveAt(int index)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function RemoveAt(index As int) As void`
			`ArgumentOutOfRangeException: Thrown if the index provided is not valid.`

## Params

| Name | Description | 
| --- | --- |
| index | The zero-based index of the item to remove. | 

## Notes

Removes the item at the specified index.

When an item is removed the items that follow the removed item, move up to occupy the vacated spot.

## Example

None.