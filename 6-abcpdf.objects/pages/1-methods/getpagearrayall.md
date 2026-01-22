# GetPageArrayAll Function

## Syntax

[C#] Page[] GetPageArrayAll() [Visual Basic] Function GetPageArrayAll() As Page()

## Params

## Notes

Gets all the Page objects under this node and descendents of this node. The pages are returned in order of page number. The Page.ID can be assigned directly to the Doc.Page property to set the focus to a particular page. For large or badly structured documents it is likely to be faster to use this type of operation than it is to repeatedly access the Doc.PageNumber property.

For an array of the immediate children of this node see GetPageArray.

## Example

None.

