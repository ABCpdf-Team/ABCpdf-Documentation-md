---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | ColorElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This class represents a color. A color consists of an array of component values. For example an RGB color has three values between zero and one, a CMYK color has four between zero and one. Colors only make sense in the context of a color space that specifies what the components represent. Most components range between zero and one. However some color spaces such as Lab have components with values outside this range. This is definitively detailed in:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 139. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorElement ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| ColorElement | Create a new ColorElement. | 
| GetColor | Get the contents of this ColorElement as an XColor. | 
| SetColor | Set the contents of this ColorElement using an XColor. | 
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
| Components | The component intensities for the color. | 
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