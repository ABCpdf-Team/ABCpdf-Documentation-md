---
title: "1-iccprofile"
css: "abcpdf-docs.css"
---

|  |  | IccProfile Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| IccProfile Constructor. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp IccProfile(ObjectSoup soup, byte[] data) IccProfile(ObjectSoup soup, string path) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup, data() As Byte) Sub New(soup As ObjectSoup, path As String) ``` `may throw Exception()` |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Params</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created IccProfile. | 
| data | An ICC profile stored in an array of bytes. | 
| path | A path to an ICC file. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| Create an IccProfile object. If the content provided is not a valid ICC profile then an exception will be thrown. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| See the PixMap.Recolor function. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>