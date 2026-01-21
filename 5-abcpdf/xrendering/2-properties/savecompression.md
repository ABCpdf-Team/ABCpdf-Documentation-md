---
title: "savecompression"
css: "abcpdf-docs.css"
---

|  |  | SaveCompression Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Compression ``` [Visual Basic] `Compression` | None | No | The preferred compression method. | 

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
      
| This property determines the preferred compression method. Not all file formats support all compression methods. Not all compression methods support all color spaces. This is why this property indicates a preferred method. The Compression enumeration accepts the following values: None [Uncompressed] G3 [G3 Black and White Fax Compression] G4 [G4 Black and White Fax Compression] LZW [LZW Compression] Jpeg [Tiff Jpeg Compression] AdobeFlate [Adobe Flate Compression] Flate [Flate Compression] PackBits [Macintosh PackBits] In general this property is most useful when producing output in formats like TIFF which support a range of color spaces and compression methods. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following example shows how to render a PDF into a multipage G4 compressed Fax TIFF using different vertical and horizontal resolutions. [C#] ```csharp using var doc = new Doc(); doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")); // set up the rendering parameters doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray; doc.Rendering.BitsPerChannel = 1; doc.Rendering.DotsPerInchX = 200; doc.Rendering.DotsPerInchY = 400; // loop through the pages int n = doc.PageCount; for (int i = 1; i [Visual Basic] ```vbnet Using doc As New Doc() doc.Read(Server.MapPath("../Rez/spaceshuttle.pdf")) ' set up the rendering parameters doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray doc.Rendering.BitsPerChannel = 1 doc.Rendering.DotsPerInchX = 200 doc.Rendering.DotsPerInchY = 400 ' loop through the pages Dim n As Integer = doc.PageCount Dim i As Integer = 1 While i 1) doc.Rendering.SaveCompression = XRendering.Compression.G4 doc.Rendering.Save(Server.MapPath("fax.tif")) System.Math.Max(System.Threading.Interlocked.Increment(i),i - 1) End While End Using ``` |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>