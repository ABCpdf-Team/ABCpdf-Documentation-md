---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | MatrixElement Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| This class represents a tranformation matrix. Transformation matrices can be used to produce affine transforms such as translations, scales, rotations and skews. A transformation matrix consists of an array of six values. Coordinates are expressed as a three element matrix:. [x, y, 1]. The transformation matrix is expressed as a three by three matrix:. [a, b, 0]. [c, d, 0]. [e, f, 1]. So to apply a matrix to a point or set of points one simply multiplies the point matrix by the transformation matrix. This is definitively detailed in:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 119. ``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.MatrixElement ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
| MatrixElement | Create a new MatrixElement. | 
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
| Elements | The six elements in this list represent the following elements of the three by three transformation matrix:. | 
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