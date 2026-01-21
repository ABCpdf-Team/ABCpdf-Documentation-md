---
title: "string"
css: "abcpdf-docs.css"
---

|  |  | String Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "0 0 0 0" | No | The rect as a string. | 

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
      
| Allows you access to the rect as a string. When working in standard PDF coordinates the format of the string is "left bottom right top". When working with top-down coordinates the format of the string is "left top right bottom". You can use the following page sizes as shortcuts when assigning a string value to an XRect: Paper Size | Width in Points | Height in Points | 
| --- | --- | --- |
| A3 | 842 | 1190 | 
| A4 | 595 | 842 | 
| A5 | 420 | 595 | 
| B4 | 729 | 1032 | 
| B5 | 516 | 729 | 
| Letter | 612 | 792 | 
| Legal | 612 | 1008 | 
| Tabloid | 792 | 1224 | 
| Ledger | 1224 | 792 | 
| Statement | 396 | 612 | 
| Executive | 540 | 720 | 
| Folio | 612 | 936 | 
| Quarto | 610 | 780 | 
| 10x14 | 720 | 1008 | 

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
      
| The following code. [C#] ```csharp var rc = new XRect(); rc.String = "10 10 200 100"; Response.Write($"Width = {rc.Width}"); Response.Write(""); Response.Write($"Height = {rc.Height}"); ``` [Visual Basic] ```vbnet Dim rc As New XRect() rc.String = "10 10 200 100" Response.Write($"Width = {rc.Width}") Response.Write("") Response.Write($"Height = {rc.Height}") ``` Produces the following output. Width = 190 Height = 90 Also see example code in: ABCpdf Text Flow Round Image Example, ABCpdf Headers and Footers Example, ABCpdf Advanced Graphics Example, ABCpdf PDF Rendering Example, Doc AddImageDoc Function, Doc AddImageFile Function, Doc AddImageObject Function, Doc MediaBox Property, Doc Rect Property, XHtmlOptions GetTagRects Function, XImage Selection Property, XRect Inset Function, XRect Magnify Function, XRect Move Function, XRect Position Function, XRect Resize Function, XRect SetRect Function, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering ColorSpace Property, XRendering DefaultHalftone Property, XRendering IccCmyk Property, XRendering SaveCompression Property, XTransform Invert Function, FontObject Widths Property, Page GetBitmap Function, TextOperation Group Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>