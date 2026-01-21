# ObjectSoupSubset Constructor

Construct an ObjectSoupSubset.

## Syntax

**[C#]**

```csharp
ObjectSoupSubset(ObjectSoup soup)
```

<span class=language>[Visual
            Basic]</span>  
`Sub New(soup As ObjectSoup)`
## Params

| Name | Description | 
| --- | --- |
| soup | The soup from which objects will be selected. | 

## Notes

Create an ObjectSoupSubset.

An ObjectSoupSubset is specific to a particular ObjectSoup and may only contain [IndirectObjects](../../1-indirectobject/default.md) from that soup.

For this reason you should specify the soup in question at the point of construction. If later you attempt to add objects from a different soup then an exception will be raised.

## Example

None.