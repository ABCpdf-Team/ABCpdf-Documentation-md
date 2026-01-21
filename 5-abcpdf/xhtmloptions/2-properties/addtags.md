---
title: "addtags"
css: "abcpdf-docs.css"
---

|  |  | AddTags Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether location of certain tags should be noted. | 

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

| This property determines whether selected elements in the HTML are noted so that their location can be determined at a later date. After adding your web pages you can retrieve information about the items on the PDF page using the GetTagIDs and the GetTagRects methods. Only HTML elements which have a visual representation can be tagged. If you are unsure if your item has a visual representation, put a border style on the element. If you can see the border then you can tag it. Using the ABCChrome engine you specify tags using attributes. Using the Gecko and MSHTML engines you specify tags using styles. The change from styles to attributes was made as the originals styles based method became standards non-compliant. The ABCChrome engine relies on JavaScript for this feature, so if you set the UseScript property to false, it will cease to operate. For the ABCChrome engine, elements with an attribute 'abcpdf-tag-visible' will be tagged. For example: ```html Gallia est omnis divisa in partes tres. ``` For the Gecko and MSHTML engines, elements of style 'abcpdf-tag-visible: true' will be tagged. For example: ```html Gallia est omnis divisa in partes tres. ``` However for the Gecko engine it is generally also a good idea to apply a border to ensure that the item is taggable. For example: ```html Gallia est omnis divisa in partes tres. ``` |  |  | 
| --- | --- | --- |

</td>
</tr>
<tr>
<td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  

Example</td>
<td width="14">&nbsp;</td>
<td valign="top">

| See the GetTagRects and the GetTagUntransformedRects methods. Also see example code in: XHtmlOptions GetTagRects Function, WebPageOperation Doc Property. |  |  | 
| --- | --- | --- |

</td>
</tr>
</tbody>
</table>