---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | IndexedColorSpaceElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This class represents an indexed color space. Indexed color spaces represent a set of colors from a palette. Each color is identified using an index into the palette. The palette itself needs to be defined in terms of another color space such as DeviceRGB or DeviceCMYK. So in many ways an indexed color space is a meta color space. This is definitively detailed in:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Section: 8.6.6.3, page 156. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorSpaceElement WebSupergoo.ABCpdf13.Elements.IndexedColorSpaceElement ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| IndexedColorSpaceElement | Create a new IndexedColorSpaceElement. | 
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
| EntryBaseColorSpace | This property represents the underlying color space for this Indexed color space. | 
| EntryHiVal | This property represents the highest number used to index into the palette. | 
| EntryLookup | This property represents the lookup table for the palette. | 
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