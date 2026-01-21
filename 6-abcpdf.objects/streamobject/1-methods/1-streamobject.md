---
title: "1-streamobject"
css: "abcpdf-docs.css"
---

|  |  | StreamObject Constructor |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| StreamObject Constructor. |  |  | 

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Syntax</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| **[C#]** ```csharp StreamObject(ObjectSoup soup) StreamObject(ObjectSoup soup, byte[] data) StreamObject(ObjectSoup soup, string path) ``` [Visual Basic] ``` Sub New(soup As ObjectSoup) Sub New(soup As ObjectSoup, data() As Byte) Sub New(soup As ObjectSoup, path As String) ``` `may throw Exception()` |  |  | 
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
| soup | The ObjectSoup to contain the newly created StreamObject. | 
| data | An array of bytes which should be placed in the StreamObject. | 
| path | A path to a file containing data which should be placed in the StreamObject. | 

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
      
| Create a StreamObject. If no arguments are passed then the StreamObject contains no data. No exception will be thrown. If an array of bytes is passed then the StreamObject data will be initialized with the contents of the array. No exception will be thrown. If a string is passed then the StreamObject data will be initialized with the contents of the file. If the file cannot be read then an exception is thrown. |  |  | 
| --- | --- | --- |

</td>
  </tr>
  <tr> 
    <td valign="top" class="sectheader">![](../../../images/steel-pin.gif)  

      Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top"> 
      
| None. |  |  | 
| --- | --- | --- |

</td>
  </tr>
</table>