# Simple Example

## Intro

Creating a PDF document is a simple process. First you create an ABCpdf Document object and then you add your content to it. You can add text, images and other kinds of graphics.

All content addition is done on the current Page and within the current Rect on that page. You can change the Page to draw on different pages and the Rect to draw in different areas. The default page is the first page and the default drawing area is the entire page.

You may find it useful to use the FrameRect method during development. This frames the current rectangle on the current page so that the area you are about to draw on is outlined.

Every time you add an item of content you will get an Object ID returned. You may wish to save these IDs and use them to query or change object properties at a later date.

## Code

First we create an ABCpdf Doc object. Next we set the font size and add some text to it. Finally we save at a specified location.

[C#] Doc theDoc = new Doc(); theDoc.FontSize = 96; theDoc.AddText("Hello World"); theDoc.Save(Server.MapPath("simple.pdf")); [Visual Basic] Dim theDoc As Doc = New Doc() theDoc.FontSize = 96 theDoc.AddText("Hello World") theDoc.Save(Server.MapPath("simple.pdf"))

## Results

simple.pdf

