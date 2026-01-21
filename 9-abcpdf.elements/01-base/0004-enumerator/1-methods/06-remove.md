---
title: "06-remove"
css: "abcpdf-docs.css"
---

# Remove Function

Remove an element from the dictionary.

## Syntax

**[C#]**

```csharp
virtual bool Remove(string key)
virtual bool Remove(TKey key)
```

<span class=language>[Visual Basic]</span>  

```
Overridable Function Remove(key As string) As Boolean
Overridable Function Remove(key As TKey) As Boolean
```

			`NullReferenceException: Thrown if the key was null.`

## Params

| Name | Description | 
| --- | --- |
| key | The name of the element to remove. | 
| return | True if the element is successfully found and removed otherwise false. | 

## Notes

Remove an element from the dictionary.

Removes the value with the specified name from the dictionary.

## Example

None.