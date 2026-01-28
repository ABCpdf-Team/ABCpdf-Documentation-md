# GetEnumerator Function

## Syntax

[C#]

```csharp
virtual <a href="../default.htm">Enumerator</a> GetEnumerator()
```

## Params

| **Name** | **Description** |
| --- | --- |
| return | An enumerator for the collection. |

## Notes

Returns an enumerator that iterates through the [DictElement](0003-dictelement_t_/default.md).

Get a KeyValuePair<string, T> enumerator for the dictionary.

DictAtom.Enumerator is a value type that implements IEnumerator<KeyValuePair<string, T>> and IDictionaryEnumerator.
