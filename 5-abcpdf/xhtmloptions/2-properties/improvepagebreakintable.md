# ImprovePageBreakInTable Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | true | No | Whether to improve the support for page break in table to prevent missing rows. | 

## Notes

The Gecko engine may truncate a table at the point that the last row on the page aligns exactly with the bottom of the page.

Set this property to true to resolve the problem.

## Example

None.