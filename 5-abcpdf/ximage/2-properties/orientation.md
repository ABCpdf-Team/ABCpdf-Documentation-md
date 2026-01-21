---
title: "orientation"
css: "abcpdf-docs.css"
---

|  |  | Orientation Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp int ``` [Visual Basic] `Integer` | See description. | Yes | The orientation of the current frame. | 

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
      
| TIFF and JPEG files can contain an Orientation setting describing how the image would be most naturally viewed. Postscript files can contain the DSC comment tag:%%Orientation: Landscape/Portraitthat describes how the image would be most naturally viewed. For Landscape orientation, this property becomes 90 degrees For example an image may be rotated by 90 degrees or flipped horizontally. These kinds of settings are most commonly used when images are scanned and orientation is only determined at a later date, perhaps via OCR. This property may take any of the following values: 0 — (a.k.a. ORIENTATION_TOPLEFT) scan lines go from top to bottom, and pixels in each scan line go from left to right. -90 — (a.k.a. ORIENTATION_TOPRIGHT) scan lines go from top to bottom, and pixels in each scan lines go from right to left. 180 — (a.k.a ORIENTATION_BOTRIGHT) scan lines go from bottom to top, and pixels in each scan lines go from right to left. -270 — (a.k.a ORIENTATION_BOTLEFT) scan lines go from bottom to top, and pixels in each scan lines go from left to right. -360 — (a.k.a ORIENTATION_LEFTTOP) scan lines go from left to right, and pixels in each scan lines go from top to bottom. 90 — (a.k.a ORIENTATION_RIGHTTOP) scan lines go from right to left, and pixels in each scan lines go from top to bottom. -180 — (a.k.a ORIENTATION_RIGHTBOT) scan lines go from right to left, and pixels in each scan lines go from bottom to top. 270 — (a.k.a ORIENTATION_LEFTBOT) scan lines go from left to right, and pixels in each scan lines go from bottom to top. By default the XImage will work with these settings to present the image the right way up. However you can select any presentation orientation by using the AppliedOrientation property to apply a transform of your choice. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr>
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>