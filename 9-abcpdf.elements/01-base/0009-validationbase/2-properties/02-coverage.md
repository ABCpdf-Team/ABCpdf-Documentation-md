# Coverage Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp HashSet ``` [Visual Basic] `HashSet` | null | No | Gets or sets the coverage. | 

## Notes

Gets or sets the coverage.

The coverage is a set of the names of the types of [Elements](../../1086-element/default.md) that have been created during validation.

The default value of this property is null which means that coverage information will not be recorded.

To record coverage information, assign a HashSet to this property.

The values in the HashSet are preserved so you can use one HashSet to determine the coverage of a group of documents.

## Example

None.