---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | Layer Class |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| A layer of visible content on a page. Each time content is added to a page a new layer is created. Different kinds of layers are created for different types of content. For example the AddText method will result in the creation of a TextLayer and the AddImage one will produce an ImageLayer. A layer corresponds to a stream object referenced from the Page Contents array. The Page.Flatten method concatenates all the stream and then compresses them to save space. Note that this type of layer is an ABCpdf construct that you cannot detect using Acrobat. Acrobat layers are something completely different and are more precisely known as Optional Content Groups (OCGs). See the Doc.Layer property for details of how to construct and manipulate this type of optional layer. ``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.StreamObject WebSupergoo.ABCpdf13.Objects.Layer WebSupergoo.ABCpdf13.Objects.GraphicLayer WebSupergoo.ABCpdf13.Objects.ImageLayer WebSupergoo.ABCpdf13.Objects.TextLayer WebSupergoo.ABCpdf13.Objects.ViewLayer ``` |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Method | Description | 
| --- | --- |
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
| BaseRect | The untransformed rect defining the bounds of the visible content on the page. | 
| Page | The Page on which the Layer is located. | 
| Rect | The transformed rect defining the bounds of the visible content. | 
| Transform | The transform which has been applied to the visible content. | 
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