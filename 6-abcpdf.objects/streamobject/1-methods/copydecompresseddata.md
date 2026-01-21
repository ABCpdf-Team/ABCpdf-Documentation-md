---
title: "copydecompresseddata"
css: "abcpdf-docs.css"
---

|  |  | CopyDecompressedData Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Copy the decompressed binary content of the stream into a byte array. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp int CopyDecompressedData() int CopyDecompressedData(byte[] destination) int CopyDecompressedData(byte[] destination, int startIndex) int CopyDecompressedData(byte[] destination, int startIndex, int maxLength) ``` [Visual Basic] ``` Function CopyDecompressedData() As Integer Function CopyDecompressedData(destination() As Byte) As Integer Function CopyDecompressedData(destination() As Byte, startIndex as Integer) As Integer Function CopyDecompressedData(destination() As Byte, startIndex as Integer, maxLength As Integer) As Integer ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| destination | The destination byte array. Default is null. | 
| startIndex | The index in the byte array at which the first byte should be written. Default is 0. | 
| maxLength | The maximum number of bytes that should be written. Default is Int.MaxValue. | 
| return | The length of the decompressed data that has been written to the array. If the destination is null then this returns the length that would have been written if a destination had been provided. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Copy the decompressed binary content of the stream into a byte array. This method does not alter the content of the StreamObject so it is an efficient way of getting the decompressed data without altering the document. If the data could not be decompressed then an exception will be raised. The decompressed data is cached so that multiple calls to this function are efficient. For this reason calling this value with a null destination is an efficient way of determining the length of the decompressed stream. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>