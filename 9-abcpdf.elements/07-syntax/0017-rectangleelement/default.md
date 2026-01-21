---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | RectangleElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This class represents a rectangle. A rectangle consists of an array of four values - two pairs of pairs. The first pair represent the x and y coordinates of the lower left of the rectangle,. the second pair represent the x and y coordinates of the upper right of the rectangle. So [lx, ly, ux, uy]. Although the pairs conventially represent the lower left and upper right corners, it is in fact legal to represent any diagaonally opposed corners and. PDF applications will automatically normalize these when they are found. This is definitively detailed in:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 88. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.RectangleElement ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| RectangleElement | Create a new RectangleElement. | 
| GetRect | Get the contents of this RectangleElement as an XRect. | 
| SetRect | Set the contents of this RectangleElement using an XRect. | 
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
| Elements | A rectangle consists of an array of four values - two pairs of pairs. | 
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