# UseScript Property

## Notes

This property determines whether JavaScript and VBScript are enabled.

By default client-side script such as JavaScript is enabled when rendering HTML documents. You may wish to change this default setting for performance or security reasons.

The ABCChrome engine relies on JavaScript for HTML analysis. If you disable it the HtmlOptions.Media, HtmlOptions.AddForms, HtmlOptions.AddTags and HtmlOptions.OnLoadScript will cease to operate. In addition the HtmlOptions.BrowserWidth zero setting, which allows the page autosize behavior, will default to the HtmlOptions.InitialWidth setting.

If you have a server edition of Windows (e.g. Windows Server 2008) and are using the MSHTML engine, you may need to also disable Enhanced Security Configuration for user running the program/application pool to allow JavaScript execution.

Script-Accessible Functions and Properties. These are functions and properties that script inside HTML can access. The function signatures shown are in C#-like syntax. You'll need to pass in the correct number of arguments.

## Syntax

[C#] bool ABCpdf_RenderWait(); [Visual Basic] Private Function ABCpdf_RenderWait() As Boolean

## Params

## Notes

## Syntax

[C#] bool ABCpdf_RenderComplete(); bool ABCpdf_RenderComplete(bool force); [Visual Basic] Private Function ABCpdf_RenderComplete() As Boolean Private Function ABCpdf_RenderComplete(ByVal force As Boolean) As Boolean

## Params

## Notes

## Examples

[C#] Doc doc = new Doc(); doc.HtmlOptions.Engine = EngineType.MSHtml; doc.HtmlOptions.UseScript = true; // Render after 3 seconds doc.HtmlOptions.OnLoadScript = "(function(){" + " window.external.ABCpdf_RenderWait();" + " setTimeout(function(){ window.external.ABCpdf_RenderComplete(); }, 3000);" + "})();"; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg.pdf")); [Visual Basic]Dim theDoc As Doc = New Doc() theDoc.HtmlOptions.Engine = EngineType.MSHtml theDoc.HtmlOptions.UseScript = True ' Render after 3 seconds theDoc.HtmlOptions.OnLoadScript = "(function(){" _ & " window.external.ABCpdf_RenderWait();" _ & " setTimeout(function(){ window.external.ABCpdf_RenderComplete(); }, 3000);" _ & "})();" theDoc.AddImageUrl("http://www.websupergoo.com") theDoc.Save(Server.MapPath("wsg.pdf"))

## Syntax

[C#] bool ABCpdf_go; [Visual Basic] Dim ABCpdf_go As Boolean

## Params

## Notes

## Examples

[C#]Doc doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Gecko; doc.HtmlOptions.UseScript = true; // Render after 3 seconds doc.HtmlOptions.OnLoadScript = "(function(){" + " window.ABCpdf_go = false;" + " setTimeout(function(){ window.ABCpdf_go = true; }, 3000);" + "})();"; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg.pdf")); [Visual Basic]Dim theDoc As Doc = New Doc() theDoc.HtmlOptions.Engine = EngineType.Gecko theDoc.HtmlOptions.UseScript = True ' Render after 3 seconds theDoc.HtmlOptions.OnLoadScript = "(function(){" _ & " window.ABCpdf_go = false;" _ & " setTimeout(function(){ window.ABCpdf_go = true; }, 3000);" _ & "})();" theDoc.AddImageUrl("http://www.websupergoo.com") theDoc.Save(Server.MapPath("wsg.pdf"))

## Syntax

[C#] void ABCChromeExt.Render(); [Visual Basic] Private Sub Render()

## Params

## Notes

Calling the method ABCChromeExt.Render() in any JavaScript executed within an HTML page will force the immediate rendering of the page to PDF without delay.

This option cannot be used in HtmlOptions.OnLoadScript - no error will occur but processing will not be curtailed.

You will need to set a sensible value for HtmlOptions.RenderDelay to allow processing to continue past the OnLoad event.

## Example

The following example shows one method of crawling and transferring an entire site to PDF. Here, we use JavaScript to determine the links present on the page. However, you could equally well use the HtmlCallback to do the same thing.

[C#] using var doc = new Doc(); string uri = "https://photojournal.jpl.nasa.gov/gallery/snt"; // Set HTML options doc.HtmlOptions.AddLinks = true; doc.HtmlOptions.UseScript = true; doc.HtmlOptions.PageCacheEnabled = false; // JavaScript is used to extract all links from the page doc.HtmlOptions.OnLoadScript = "var hrefCollection = document.all ? document.all.tags(\"a\") : document.getElementsByTagName(\"a\");" + "var allLinks = \"\";" + "for(i = 0; i < hrefCollection.length; ++i) {" + "if (i > 0)" + " allLinks += \",\";" + "allLinks += hrefCollection.item(i).href;" + "};" + "document.documentElement.abcpdf = allLinks;"; // Array of links - start with base URL var links = new ArrayList(); links.Add(uri); for (int i = 0; i < links.Count; i++) { // Stop if we render more than 20 pages if (doc.PageCount > 20) break; // Add page doc.Page = doc.AddPage(); int id = doc.AddImageUrl(links[i] as string); // Links from the rendered page string allLinks = doc.HtmlOptions.GetScriptReturn(id); string[] newLinks = allLinks.Split(new char[] { ',' }); foreach (string link in newLinks) { // Check to see if we allready rendered this page if (links.BinarySearch(link) < 0) { // Skip links inside the page int pos = link.IndexOf("#"); if (!(pos > 0 && links.BinarySearch(link.Substring(0, pos)) >= 0)) { if (link.StartsWith(uri)) { links.Add(link); } } } } // Add other pages while (true) { doc.FrameRect(); if (!doc.Chainable(id)) break; doc.Page = doc.AddPage(); id = doc.AddImageToChain(id); } } // Link pages together doc.HtmlOptions.LinkPages(); // Flatten all pages for (int i = 1; i <= doc.PageCount; i++) { doc.PageNumber = i; doc.Flatten(); } // Save the document doc.Save(Server.MapPath("HtmlOptionsJavaScript.pdf")); [Visual Basic] Using doc As New Doc() Dim theURL As String = "https://photojournal.jpl.nasa.gov/gallery/snt" ' Set HTML options doc.HtmlOptions.AddLinks = True doc.HtmlOptions.UseScript = True doc.HtmlOptions.PageCacheEnabled = False ' JavaScript is used to extract all links from the page doc.HtmlOptions.OnLoadScript = "var hrefCollection = document.all ? document.all.tags(""a"") : document.getElementsByTagName(""a"");" + "var allLinks = """";" + "for(i = 0; i < hrefCollection.length; ++i) {" + "if (i > 0)" + vbTab & "allLinks += "","";" + "allLinks += hrefCollection.item(i).href;" + "};" + "document.documentElement.abcpdf = allLinks;" ' Array of links - start with base URL Dim links As New ArrayList() links.Add(theURL) Dim i As Integer = 0 While i < links.Count ' Stop if we render more than 20 pages If doc.PageCount > 20 Then Exit While End If ' Add page doc.Page = doc.AddPage() Dim theID As Integer = doc.AddImageUrl(TryCast(links(i), String)) ' Links from the rendered page Dim allLinks As String = doc.HtmlOptions.GetScriptReturn(theID) Dim newLinks As String() = allLinks.Split(New Char() {","C}) For Each link As String In newLinks ' Check to see if we allready rendered this page If links.BinarySearch(link) < 0 Then ' Skip links inside the page Dim pos As Integer = link.IndexOf("#") If Not (pos > 0 AndAlso links.BinarySearch(link.Substring(0, pos)) >= 0) Then If link.StartsWith(theURL) Then links.Add(link) End If End If End If Next ' Add other pages While True doc.FrameRect() If Not doc.Chainable(theID) Then Exit While End If doc.Page = doc.AddPage() theID = doc.AddImageToChain(theID) End While System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While ' Link pages together doc.HtmlOptions.LinkPages() ' Flatten all pages Dim i As Integer = 1 While i <= doc.PageCount doc.PageNumber = i doc.Flatten() System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While ' Save the document doc.Save(Server.MapPath("HtmlOptionsJavaScript.pdf")) End Using

Also see example code in: ABCpdf Paged HTML Example.

