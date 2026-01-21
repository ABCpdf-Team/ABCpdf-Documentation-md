---
title: "colorspace"
css: "abcpdf-docs.css"
---

|  |  | ColorSpace Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp XRendering.ColorSpaceType ``` [Visual Basic] `XRendering.ColorSpaceType` | XRendering.ColorSpaceType.Rgb | No | The name of the output color space. | 

</td>

                <td width="60">&nbsp;</td>

                <td>&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>

      <tr>
        <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  

        Notes</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| The name of the output color space. The XRendering.ColorSpaceType enumeration may take the following values: Rgb - red, green and blue Gray - grayscale Cmyk - cyan, magenta, yellow and black Lab - a device independent color space Indexed - indexed RGB; see the Palette property The following table shows the supported color spaces and valid BitsPerChannel for each output format: Output format | RGB | Gray | CMYK | Lab | Indexed | 
| --- | --- | --- | --- | --- | --- |
| TIFF | 8, 16 | 1, 8, 16 | 8, 16 | 8, 16 |  | 
| PSD (Photoshop) | 8, 16 | 8, 16 | 8, 16 | 8, 16 |  | 
| JP2 (JPEG 2000) | 8, 16 | 8, 16 | 8, 16 |  |  | 
| JPG | 8 | 8 | 8 |  |  | 
| BMP | 8 | 8 |  |  | 8 | 
| PNG | 8 | 8, 16 |  |  | 8 | 
| GIF | 8 (8 bit indexed) | 8 |  |  | 8 | 

</td>

                <td width="60">&nbsp;</td>

                <td width="11">&nbsp;</td>
              </tr>
            </tbody>
          </table>
        </td>
      </tr>

      <tr>
        <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>

        <td width="14">&nbsp;</td>

        <td valign="top">
          
| The following example shows the effect that this parameter has on PDF rendering. [C#] ```csharp using var doc = new Doc(); doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg")); doc.Rect.String = doc.MediaBox.String; // Render document in Gray colorspace doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray; doc.Rendering.DotsPerInch = 36; doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.AddImage(Server.MapPath("../mypics/Shuttle.jpg")) doc.Rect.String = doc.MediaBox.[String] ' Render document in Gray colorspace doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Gray doc.Rendering.DotsPerInch = 36 doc.Rendering.Save(Server.MapPath("RenderingColorSpace.png")) End Using ``` Shuttle.jpg RenderingColorSpace.png Also see example code in: XRendering DefaultHalftone Property, XRendering IccCmyk Property, XRendering Overprint Property, XRendering SaveCompression Property. |  |  | 
| --- | --- | --- |

</td>
      </tr>
    </tbody>
  </table>