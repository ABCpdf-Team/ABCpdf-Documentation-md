# ForWebKit Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IHtmlWebKitOptions ``` [Visual Basic] `IHtmlWebKitOptions` | n/a | Yes | An object that provides access to only the HTML options supported by the ABCWebKit engine. | 

## Notes

The HTML options supported by the ABCWebKit engine.

### Supported methods

- [EndTasks](../1-methods/endtasks.md)

### Supported properties

- [AddLinks](addlinks.md)
- [BrowserWidth](browserwidth.md)
- [FireShield](fireshield.md)
- [HideBackground](hidebackground.md)
- [Media](media.md)
- [OnLoadScript](onloadscript.md)
- [ProcessOptions](processoptions.md)
- [RepaintTimeout](repainttimeout.md) [but not RepaintDelay]
- [RetryCount](retrycount.md)
- [Timeout](timeout.md)
- [UseScript](usescript.md)

## Example

[C#]

```csharp
using var doc = new Doc();
doc.HtmlOptions.Engine = EngineType.WebKit;
doc.HtmlOptions.ForWebKit.AddLinks = true;

// You can store a reference to the filter to reduce code repetition
var options = doc.HtmlOptions.ForWebKit;

options.UseScript = false;

doc.AddImageUrl("http://www.websupergoo.com");
doc.Save(Server.MapPath("wsg4.pdf"));
```

<span class=language>[Visual Basic]</span>
```vbnet
Using doc As New Doc()
  doc.HtmlOptions.Engine = EngineType.WebKit
  doc.HtmlOptions.ForWebKit.AddLinks = True

  ' You can store a reference to the filter to reduce code repetition
  Dim options As IHtmlWebKitOptions = doc.HtmlOptions.ForWebKit

  options.UseScript = False

  doc.AddImageUrl("http://www.websupergoo.com")
  doc.Save(Server.MapPath("wsg4.pdf"))
End Using
```