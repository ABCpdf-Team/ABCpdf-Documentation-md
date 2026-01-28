# Remove Function

## Syntax

[C#] bool Remove(IndirectObject value)

## Params

## Notes

When an object is removed it leaves a gap in the Soup. Other objects do not move to fill the gap.

RefAtoms pointing to the object which was removed are not updated. This means you can remove one object and replace it with a substitute. Other IndirectObjects in the Soup will then refer to the new object rather than the old one.

However it also means that you should be careful about removing an object and not replacing it. Because the slot is free it may be re-used and any references which exist may then point to a new - inappropriate - object.

## Example

None.

