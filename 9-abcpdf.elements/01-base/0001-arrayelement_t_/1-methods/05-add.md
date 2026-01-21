# Add Function

Add an [Element](../../1086-element/default.md) to the end of the array.

## Syntax

**[C#]**

```csharp
virtual void Add(T value)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function Add(value As T) As void`
			`NullReferenceException: Thrown if an attempt is made to insert a null value in a non-Nullable array.`

## Params

| Name | Description | 
| --- | --- |
| value | The value. | 

## Notes

Add an [Element](../../1086-element/default.md) to the end of the array.

This method adds an [Element](../../1086-element/default.md) to the array.

Most [ArrayElements](../default.md) cannot hold null values in a meaningful way. So in general, if you provide a null value this will result in an exception being raised.

Occasionally it is appropriate for [ArrayElements](../default.md) to hold null values represented as NullAtoms. You can indicate this is acceptable, by setting the [Nullable](../2-properties/03-nullable.md) property.

## Example

None.