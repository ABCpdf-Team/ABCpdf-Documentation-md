---
title: "01-entrytarget"
css: "abcpdf-docs.css"
---

|  |  | EntryTarget Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp Element ``` [Visual Basic] `Element` | null | No | This property represents the destination target. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| This property represents the destination target. It is a required entry and defined as part of the PDF 1.0 specification. The Target may be a PageObjectElement or, in the case of a remote destination, an Element containing a NumAtom indicating a page number. In this case page numbers use a zero rather than one based index. In a PDF 2.0 document this property may be a StructureElementElement indicating the part of the document to which the destination refers. For definitive details see:. The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 151, page 366. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>