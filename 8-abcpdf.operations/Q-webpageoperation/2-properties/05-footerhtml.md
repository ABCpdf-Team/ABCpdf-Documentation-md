# FooterHtml Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp string ``` [Visual Basic] `string` | null | No | Any HTML footer required for the page. | 

## Notes

Any HTML footer required for the page.

Ensure you have set an appropriate margin at the bottom of the page if you want to use this property.

The HTML content area is defined by the Doc.Rect. Headers go above the Doc.Rect. Footers go below it.

As such if you set footers you need to ensure that you leave sufficient room between the bottom of the Doc.Rect and the bottom of the Doc.MediaBox.

There are special HTML tags you can use to insert pre-defined content.

- 
- 
- 
- 
- 

## Example

None.
            Also see example code in: [WebPageOperation Doc Property](01-doc.md).