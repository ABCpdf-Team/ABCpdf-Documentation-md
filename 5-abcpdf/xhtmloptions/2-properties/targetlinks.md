# TargetLinks Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether hyperlinks should be allowed to open new windows. | 

## Notes

Whether hyperlinks with targets should be allowed to open in a new browser window.

In HTML, hyperlinks whose targets are neither empty, "_self", "_parent", nor "_top" will be opened in new browser window.

Setting this property to true allows you to mimic this behavior when the PDF document is viewed inside a browser.

## Example

None.