# Paged HTML Example

## Setup

We first create a Doc object and inset the edges a little so that the HTML will appear in the middle of the page.

[C#] using var doc = new Doc(); doc.Rect.Inset(72, 144); [Visual Basic] Using doc As New Doc() doc.Rect.Inset(72, 144)

## Features

We set some HTML options to choose the HTML engine and features we are interested in. The defaults assigned here are set up for ease of development and you may wish to change some for release.

[C#] doc.HtmlOptions.Engine = EngineType.Chrome123; doc.HtmlOptions.UseScript = true; // enable JavaScript doc.HtmlOptions.Media = MediaType.Print; // Or Screen for a more screen oriented output doc.HtmlOptions.InitialWidth = 800; // In case we have a responsive site which is non-specific on good widths //doc.HtmlOptions.RepaintDelay = 500; // Only required if you have AJAX or animated content such as graphs //doc.HtmlOptions.IgnoreCertificateErrors = false; // Disabled for ease of debugging //doc.HtmlOptions.FireShield.Policy = XHtmlFireShield.Enforcement.Deny; // Disabled for ease of debugging [Visual Basic] doc.HtmlOptions.Engine = EngineType.Chrome123 doc.HtmlOptions.UseScript = True ' enable JavaScript doc.HtmlOptions.Media = MediaType.Print ' Or Screen for a more screen oriented output doc.HtmlOptions.InitialWidth = 800 ' In case we have a responsive site which is non-specific on good widths 'doc.HtmlOptions.RepaintDelay = 500; // Only required if you have AJAX or animated content such as graphs 'doc.HtmlOptions.IgnoreCertificateErrors = false; // Disabled for ease of debugging 'doc.HtmlOptions.FireShield.Policy = XHtmlFireShield.Enforcement.Deny; // Disabled for ease of debugging

## Page

We add the first page of HTML. We save the returned ID as this will be used to add subsequent pages.

[C#]doc.Page = doc.AddPage(); int id = doc.AddImageUrl("http://www.yahoo.com/"); [Visual Basic] doc.Page = doc.AddPage() Dim theID As Integer theID = doc.AddImageUrl("http://www.yahoo.com/")

## Chain

We now chain subsequent pages together. We stop when we reach a page which wasn't truncated.

[C#]while (true) { doc.FrameRect(); // add a black border if (!doc.Chainable(id)) break; doc.Page = doc.AddPage(); id = doc.AddImageToChain(id); } [Visual Basic] While True doc.FrameRect() ' add a black border If Not doc.Chainable(theID) Then Exit While End If doc.Page = doc.AddPage() theID = doc.AddImageToChain(theID) End While

## Flatten

After adding the pages we can flatten them. We can't do this until after the pages have been added because flattening will invalidate our previous ID and break the chain.

[C#]for (int i = 1; i <= doc.PageCount; i++) { doc.PageNumber = i; doc.Flatten(); } [Visual Basic] Dim i As Integer = 1 While i <= doc.PageCount doc.PageNumber = i doc.Flatten() System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While

## Save

Finally we save.

[C#]doc.Save(Server.MapPath("pagedhtml.pdf")); [Visual Basic] doc.Save(Server.MapPath("pagedhtml.pdf")) End Using

## Results

We get the following output.

