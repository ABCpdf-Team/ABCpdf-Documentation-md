---
title: "addxobject"
css: "abcpdf-docs.css"
---

|  |  | AddXObject Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Add a Form or Image XObject to the current page. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int AddXObject(Objects.PixMap pm) int AddXObject(Objects.FormXObject pm) ``` [Visual Basic] ``` Function AddXObject(pm As Objects.PixMap) As Integer Function AddXObject(pm As Objects.FormXObject) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| pm | The image to be added to the page. | 
| return | The Object ID of the newly added Image Object. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Add a Form or Image XObject into the current rectangle on the current page. Form and Image XObjects represent a drawing sequence external to the main content stream of the page. Image XObjects represent a raster bitmap in one of a variety of color spaces. Form XObjects represent a separate content stream with a separate sequence of drawing commands. For example a Form XObject might be used to represent a "Draft" stamp which might then be applied on various pages at various locations. The fact that this stamp is an external object allows the viewing application to cache the representation and also allows changes to the stamp to affect the appearance of multiple instances. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This example shows how to load an image into a PixMap and then draw it on the current page using the AddXObject method. [C#] ```csharp using var doc = new Doc(); doc.Rect.Inset(50, 50); doc.Transform.Rotate(20, 200, 200); doc.Color.SetRgb(200, 200, 255); doc.FillRect(); var pm = new PixMap(doc.ObjectSoup); using var img = (Bitmap)Bitmap.FromFile(Server.MapPath("mypics/mypic.png")); pm.SetBitmap(img, true); doc.AddXObject(pm); doc.Save(Server.MapPath("examplePixMapBitmap.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Rect.Inset(50, 50) doc.Transform.Rotate(20, 200, 200) doc.Color.SetRgb(200, 200, 255) doc.FillRect() Dim pm As New PixMap(doc.ObjectSoup) Dim img As Bitmap = DirectCast(Bitmap.FromFile(Server.MapPath("mypics/mypic.png")), Bitmap) pm.SetBitmap(img, True) doc.AddXObject(pm) doc.Save(Server.MapPath("examplePixMapBitmap.pdf")) End Using ``` examplePixMapBitmap.pdf |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>