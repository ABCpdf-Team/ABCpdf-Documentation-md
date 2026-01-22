# Remove Function

Remove an element from the dictionary.

## Syntax

[C#]

```csharp
virtual bool Remove(string key)virtual bool Remove(TKey key)
```

[Visual Basic]

```vb
Overridable Function Remove(key As string) As BooleanOverridable Function Remove(key As TKey) As Boolean
```

## Params

| **Name** | **Description** |
| --- | --- |
| key | The name of the element to remove. |
| return | True if the element is successfully found and removed otherwise false. |

## Notes

Remove an element from the dictionary.

Removes the value with the specified name from the dictionary.
