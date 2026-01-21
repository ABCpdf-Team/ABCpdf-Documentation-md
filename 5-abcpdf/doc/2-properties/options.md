---
title: "options"
css: "abcpdf-docs.css"
---

|  |  | Options Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic] `String` | "" | No | The state options for low level drawing control. | 

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
      
| The options property is an advanced feature which allows low level control over PDF drawing. It is important to use it correctly as incorrect use can corrupt your documents. The value of the options property is inserted into the PDF content stream after state has been established but before any drawing has taken place. You can use this property to insert your own state commands. This is most commonly used for drawing dashed lines. FillRect, FrameRect, AddLine and AddArc all insert the options parameter. You can find details of graphics state parameters and how to use them in the Adobe PDF Specification. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| The following code adds an arc to a document. It uses the options parameter to make the line dashed rather than solid. [C#] ```csharp using var doc = new Doc(); doc.Width = 24; doc.Color.String = "0 120 0"; doc.Options = "[6 10] 6 d"; doc.AddArc(0, 270, 300, 400, 200, 300); doc.Save(Server.MapPath("docoptions.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.Width = 24 doc.Color.String = "0 120 0" doc.Options = "[6 10] 6 d" doc.AddArc(0, 270, 300, 400, 200, 300) doc.Save(Server.MapPath("docoptions.pdf")) End Using ``` docoptions.pdf |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>