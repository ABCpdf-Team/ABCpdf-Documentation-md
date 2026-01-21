# TryGetValue Function

Gets the value associated with the specified key.

## Syntax

**[C#]**

```csharp
virtual bool TryGetValue(string key, out value)
virtual bool TryGetValue(TKey key, out value)
```

<span class=language>[Visual Basic]</span>  

```
Overridable Function TryGetValue(key As string, value As out) As Boolean
Overridable Function TryGetValue(key As TKey, value As out) As Boolean
```

## Params

| Name | Description | 
| --- | --- |
| key | The key of the value to get. | 
| value | When this method returns this contains the value associated with the specified key. If the key was not found this contains the default value for the type of the value. | 
| return | True if the DictElement contains the specified key otherwise false. | 

## Notes

Gets the value associated with the specified key.

## Example

None.