---
title: "20-systemdrawing"
css: "abcpdf-docs.css"
---

|  |  | System.Drawing Example |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
|  |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Intro</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This example shows how to port System.Drawing code for output to PDF. You may have System.Drawing code which writes output to the screen or an image or to a printer. You may wish to modify this code to write to a PDF. ABCpdf comes with wrapper code which can significantly ease this process. You can find a full example project including the wrapper classes under the ABCpdf menu item. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Basics</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The wrapper contains the following namespaces: ```csharp using WebSupergoo.ABCpdf13.Drawing; using WebSupergoo.ABCpdf13.Drawing.Drawing2D; using WebSupergoo.ABCpdf13.Drawing.Text; ``` These contain classes which are direct analogues for the classes contained in the System.Drawing namespaces. For example, a System.Drawing.Pen maps to a WebSupergoo.ABCpdf13.Drawing.Pen and a System.Drawing.Bitmap maps to a WebSupergoo.ABCpdf13.Drawing.Bitmap. The procedure for porting your System.Drawing code is simple: Change namespaces from those in System.Drawing to the corresponding ones in ABCpdf13.Drawing (Drawing, Drawing.Text, Drawing.Drawing2D etc.) Change all types from those in System.Drawing to the corresponding types in ABCpdf13.Drawing (Pen, Brush, Color etc.) Remove any code which does not have an analogues in ABCpdf.Drawing In general, the number of calls which do not have analogues in ABCpdf.Drawing should be small. However, we provide the full source code for System.Drawing so extending the assembly is simple. As well as the standard functions analogous to those in System.Drawing, the ABCpdf13.Drawing namespace also contains similar functions aimed at greater control over the PDF production process. For example, the ABCpdf Color class contains a FromCmyk function to allow the construction of CMYK colors as well as RGB ones. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Original </TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| We start with our source System.Drawing code. [C#] ```csharp // create a canvas for painting on Bitmap pg = new Bitmap((int)(8.5 * 72), (int)(11 * 72)); Graphics gr = Graphics.FromImage(pg); // clear the canvas to white Rectangle pgRect = new Rectangle(0, 0, pg.Width, pg.Height); SolidBrush solidWhite = new SolidBrush(Color.White); gr.FillRectangle(solidWhite, pgRect); // load a new image and draw it centered on our canvas Stream stm = Assembly.GetExecutingAssembly().GetManifestResourceStream("Examples.pic1.jpg"); Image img = Image.FromStream(stm); int w = img.Width * 2; int h = img.Height * 2; Rectangle rc = new Rectangle((pg.Width - w) / 2, (pg.Height - h) / 2, w, h); gr.DrawImage(img, rc); img.Dispose(); stm.Close(); // frame the image with a black border gr.DrawRectangle(new Pen(Color.Black, 4), rc); // add some text at the top left of the canvas Font fn = new Font("Comic Sans MS", 72); SolidBrush solidBlack = new SolidBrush(Color.Black); gr.DrawString("My Picture", fn, solidBlack, (int)(pg.Width * 0.1), (int)(pg.Height * 0.1)); // save the output pg.Save("../../abcpdf.drawing.gif", System.Drawing.Imaging.ImageFormat.Gif); ``` [Visual Basic] ```vbnet Imports WebSupergoo.ABCpdf13.Drawing; Imports WebSupergoo.ABCpdf13.Drawing.Drawing2D; Imports WebSupergoo.ABCpdf13.Drawing.Text; ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Names</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| First, we swap out the old System.Drawing namespaces and insert our own ABCpdf.Drawing ones. Note that ABCpdf.Drawing uses structures like rectangles and points which are defined in System.Drawing. So, we create aliases to make it easy to reference them. [C#] ```csharp using System; using System.IO; using System.Reflection; using WebSupergoo.ABCpdf13.Drawing; using WebSupergoo.ABCpdf13.Drawing.Drawing2D; using WebSupergoo.ABCpdf13.Drawing.Text; using Rectangle = System.Drawing.Rectangle; using RectangleF = System.Drawing.RectangleF; using Point = System.Drawing.Point; using PointF = System.Drawing.PointF; ``` [Visual Basic] ```vbnet Imports System; Imports System.IO; Imports System.Reflection; Imports WebSupergoo.ABCpdf13.Drawing; Imports WebSupergoo.ABCpdf13.Drawing.Drawing2D; Imports WebSupergoo.ABCpdf13.Drawing.Text; Imports Rectangle = System.Drawing.Rectangle; Imports RectangleF = System.Drawing.RectangleF; Imports Point = System.Drawing.Point; Imports PointF = System.Drawing.PointF; ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Create</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Because we're drawing on a page of a PDF document rather than on an image, we need to make a few modifications to the first lines of code. [C#] ```csharp // create a canvas for painting on var doc = new PDFDocument(); var pg = doc.AddPage((int)(8.5 * 300), (int)(11 * 300)); var gr = pg.Graphics; ``` [Visual Basic] ```vbnet ' create a canvas for painting on Dim doc As New PDFDocument() Dim pg = doc.AddPage(DirectCast(8.5 * 300, Integer), DirectCast(11 * 300, Integer)) Dim gr = pg.Graphics ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Draw</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The drawing code remains completely unchanged. [C#] ```csharp // clear the canvas to white var pgRect = new Rectangle(0, 0, pg.Width, pg.Height); var solidWhite = new SolidBrush(Color.White); gr.FillRectangle(solidWhite, pgRect); // load a new image and draw it centered on our canvas using var stm = File.OpenRead(Server.MapPath("mypics/pic1.jpg")); using var img = Image.FromStream(stm); int w = img.Width; int h = img.Height; Rectangle rc = new Rectangle((pg.Width - w) / 2, (pg.Height - h) / 2, w, h); gr.DrawImage(img, rc); // frame the image with a black border gr.DrawRectangle(new Pen(Color.Black, 4), rc); // add some text at the top left of the canvas Font fn = new Font("Comic Sans MS", 300); var solidBlack = new SolidBrush(Color.Black); gr.DrawString("My Picture", fn, solidBlack, (int)(pg.Width * 0.1), (int)(pg.Height * 0.1)); ``` [Visual Basic] ```vbnet ' clear the canvas to white Dim pgRect As New Rectangle(0, 0, pg.Width, pg.Height) Dim solidWhite As New SolidBrush(Color.White) gr.FillRectangle(solidWhite, pgRect) ' load a new image and draw it centered on our canvas Dim stm As Stream = File.OpenRead(Server.MapPath("mypics/pic1.jpg")) Dim img As Image = Image.FromStream(stm) Dim w As Integer = img.Width Dim h As Integer = img.Height Dim rc As New Rectangle((pg.Width - w) / 2, (pg.Height - h) / 2, w, h) gr.DrawImage(img, rc) img.Dispose() stm.Close() ' frame the image with a black border gr.DrawRectangle(New Pen(Color.Black, 4), rc) ' add some text at the top left of the canvas Dim fn As New Font("Comic Sans MS", 300) Dim solidBlack As New SolidBrush(Color.Black) gr.DrawString("My Picture", fn, solidBlack, DirectCast(pg.Width * 0.1, Integer), DirectCast(pg.Height * 0.1, Integer)) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Save</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Because we're saving to a PDF document, we need to make a few modifications to the last lines of code. [C#] ```csharp // save the output doc.Save(Server.MapPath("abcpdf.drawing.pdf")); ``` [Visual Basic] ```vbnet ' save the output doc.Save(Server.MapPath("abcpdf.drawing.pdf")) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../images/steel-pin.gif)  
Results</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| abcpdf.drawing.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>