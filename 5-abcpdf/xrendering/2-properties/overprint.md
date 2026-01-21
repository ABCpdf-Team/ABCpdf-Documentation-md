---
title: "overprint"
css: "abcpdf-docs.css"
---

|  |  | Overprint Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to apply overprint. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Overprint is a way of combining colors when dealing with subtractive color spaces such as CMYK or DeviceN. Normally when one color is painted over another it replaces the underlying color. So a yellow over a magenta becomes yellow. If Overprint is set, then the top color may be placed over the top of the base color. So yellow over magenta becomes a mixture of both yellow and magenta inks, which creates red. This can be useful for printing purposes. If Overprint is true, and NamedSeparation is blank, an overprint preview is created that is designed to simulate the look of a document when inks are overprinted according to the details in the pdf. For more information on overprinting, please see the Adobe PDF Specification. Acrobat Display. The default overprint settings are subtly different in Acrobat than in other common viewers like Chrome. Acrobat allows you to choose whether to simulate overprint or not. The settings for this are under the Page Display preferences. The default value for this is "Only For PDF/X Files" so if a file is seen to be is PDF/X, then overprint will be automatically set to true. This is a little different from ABCpdf, Chrome and other common viewers, which have a default value of false. If you wish to detect PDF/X files so that you can set the overprint flag, simply use a function of the following form. [C#] ```csharp bool IsPdfX(Doc doc) { var cat = doc.ObjectSoup.Catalog; var xmp = cat.Metadata != null ? cat.Metadata.GetText() : ""; if (xmp.Contains("GTS_PDFXVersion")) return true; var trailer = doc.ObjectSoup.Trailer; var info = cat.Resolve(Atom.GetItem(trailer.Atom, "Info")) as DictAtom; return info != null && info.Contains("GTS_PDFXVersion");} ``` [Visual Basic] ```vbnet Function IsPdfX(ByVal doc As Doc) As Boolean Dim cat = doc.ObjectSoup.Catalog Dim xmp = If(cat.Metadata IsNot Nothing, cat.Metadata.GetText(), "") If xmp.Contains("GTS_PDFXVersion") Then Return True Dim trailer = doc.ObjectSoup.Trailer Dim info = TryCast(cat.Resolve(Atom.GetItem(trailer.Atom, "Info")), DictAtom) Return info IsNot Nothing AndAlso info.Contains("GTS_PDFXVersion")End Function ``` | 
| --- |

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); // Open document with overprint doc.Read(Server.MapPath("../mypics/Overprint.pdf")); // Render the document (we need to go to CMYK for overprint) doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk; doc.Rendering.Overprint = true; doc.Rendering.IccRgb = "device"; doc.Rendering.IccGray = "device"; doc.Rendering.IccCmyk = "device"; doc.Rendering.IccOutput = "device"; // Put image back into another PDF and render the document as RGB // (so that we can see the effect of the overprint in RGB) using var theRgb = new Doc(); theRgb.AddImageData(doc.Rendering.GetData(".tif"), 1); theRgb.Rendering.DotsPerInch = 36; theRgb.Rendering.ColorSpace = XRendering.ColorSpaceType.Rgb; theRgb.Rendering.Save(Server.MapPath("RenderingOverprint.png")); ``` [Visual Basic] ```vbnet Using doc As New Doc() ' Open document with overprint doc.Read(Server.MapPath("../mypics/Overprint.pdf")) ' Render the document (we need to go to CMYK for overprint) doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk doc.Rendering.Overprint = True doc.Rendering.IccRgb = "device" doc.Rendering.IccGray = "device" doc.Rendering.IccCmyk = "device" doc.Rendering.IccOutput = "device" ' Put image back into another PDF and render the document as RGB ' (so that we can see the effect of the overprint in RGB) Dim theRgb As New Doc() theRgb.AddImageData(doc.Rendering.GetData(".tif"), 1) doc.Clear() theRgb.Rendering.DotsPerInch = 36 theRgb.Rendering.ColorSpace = XRendering.ColorSpaceType.Rgb theRgb.Rendering.Save(Server.MapPath("RenderingOverprint.png")) theRgb.Clear() End Using ``` RenderingOverprint.png |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>