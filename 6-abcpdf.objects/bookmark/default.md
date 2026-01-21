# Bookmark Class

A bookmark or outline item.

PDF documents typically provide a list of bookmarks for easy navigation between pages. In Acrobat this navigation structure is available under the Bookmarks tab. The PDF specification refers to this structure as the document outline.

The document outline comprises of a hierarchy of bookmarks. The bookmark at the top of the hierarchy is available via the [Doc.Bookmark](../../5-abcpdf/doc/2-properties/bookmark.md) property. Typically a bookmark triggers navigation to a particular page but in some cases it may trigger a different and more complex type of action.

Every bookmark holds a collection of all its child bookmarks. As with all collections you can use the Count property to determine the number of items contained and you can iterate through the collection using the standard methods appropriate to the language you are coding in.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.Bookmark ```

`Implements: IList, ICollection, IEnumerable, IList, ICollection, IEnumerable`

## Method Description CopyTo Copies the Bookmarks into an array. Add Adds a Bookmark to the end of the list. Clear Removes all Bookmarks from the list. Contains Determines whether the list contains a specific Bookmark. IndexOf Determines the index of a specific Bookmark. &nbsp;Insert Inserts a Bookmark into the list at the specified position. Remove Removes a Bookmark from the list. RemoveAt Remove the Bookmark at the specified location. GetEnumerator Gets an enumerator for the Collection. &nbsp;Adopt Adopt a specified Bookmark. Refresh Refresh and reload the document Bookmarks. &nbsp; inherited methods... &nbsp;

## Property Description Count The number of Bookmarks in the collection. &nbsp;Item Get or set the Bookmark at the specified index. Open Whether the bookmark appears open or closed. Page The destination Page associated with this bookmark. PageID The destination Page ID associated with this bookmark. Parent The parent of this Bookmark. Title The bookmark title to be displayed on screen. &nbsp; inherited properties...