# GetContentData Function

## Syntax

[C#] byte[] GetContentData() byte[] GetContentData(StreamObject[] contents)

## Params

## Notes

Gets the decompressed content data from the page.

If the page contains multiple content streams then the data from these will be concatenated so you can treat them as one.

However, while the data is concatenated, the streams are left untouched - the function does not alter the page.

If a content stream could not be decompressed then an exception will be raised.

If you need to go through all the content streams associated with a set of pages, the ContentStreamOperation class provides this type of functionality.

## Example

None.

