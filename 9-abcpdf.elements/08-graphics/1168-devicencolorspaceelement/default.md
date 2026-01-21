---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | DeviceNColorSpaceElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This class represents a DeviceN or multi-separation color space. A DeviceN color space represents a set of custom colors. Most typically these are spot colors used in printing. For example the conventional color space for printing is CMYK and for that you can use the DeviceCMYK color space. However processes like Hexachrome added orange and green inks to better represent a wider range of colors. Using a DeviceN color space you can specify a CMYKOG color space which will print correctly on a Hexachrome printer. The DeviceN color space includes a conversion function so that it will also provide a good representation on screen and on normal CMYK printers. This is definitively detailed in:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Section: 8.6.6.5, page 159. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorSpaceElement WebSupergoo.ABCpdf13.Elements.DeviceNColorSpaceElement ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| DeviceNColorSpaceElement | Create a new DeviceNColorSpaceElement. | 
|  | inherited methods... | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Property | Description | 
| --- | --- |
| EntryNames | This property represents the names of the colors within the DeviceN color space. | 
| EntryAlternateColorSpace | This property represents the alternate color space for this DeviceN color space. | 
| EntryTintTransform | This property represents the tint transform function. | 
| EntryAttributes | This property represents addition attributes specific to this color space. | 
|  | inherited properties... | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
        <tr> 
          <td>&nbsp; </td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
</table>