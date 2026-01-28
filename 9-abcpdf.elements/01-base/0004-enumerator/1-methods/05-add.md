# Add Function

Adds the specified key and value to the dictionary.

## Syntax

[C#]

```csharp
virtual void Add(string key, T value)virtual void Add(TKey key, TVal value)
```

## Params

| **Name** | **Description** |
| --- | --- |
| key | The key of the element to add. |
| value | The value of the element to add. |

## Notes

Adds the specified key and value to the dictionary.

This method adds an item to the dictionary.

If the key or value is null then this method will throw an ArgumentNullException. If the key is already present in the dictionary then this method will throw an ArgumentException.
