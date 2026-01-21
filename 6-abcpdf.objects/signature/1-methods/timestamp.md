---
title: "timestamp"
css: "abcpdf-docs.css"
---

|  |  | Timestamp Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Sign a document timestamp signature field using a Timestamping Authority (TSA). |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void Timestamp(Oid oid, int reserve) virtual void Timestamp(Oid oid, DataType dataType, int reserve) ``` [Visual Basic] ``` Overridable Sub Timestamp(oid As Oid, reserve As int) Overridable Sub Timestamp(oid As Oid, dataType as DataType, reserve As int) ``` ``` may throw Exception() ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| oid | The hash algorithm to use to create the digest of the document data, for example new Oid("SHA256"). | 
| reserve | The number of bytes to reserve for the returned signed timestamp data. A typical value might be in the region of 5000. If the value is too small an exception will be raised. This value is only relevant if you are using a CustomSigner. | 
| dataType | The type of data to be passed to the CustomSigner and expected back from it. This value is only relevant if you are using a CustomSigner or CustomSigner2. For details of the possible values and what they mean, see the Sign method. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Sign a document timestamp signature field using a Timestamping Authority (TSA). The signature must be an unsigned RFC 3161 timestamp signature. If you need to create such a signature you can do so using the XForm.AddDocTimestamp method. You need to set one of either the TimestampServiceUrl or the CustomSigner properties before calling this function. The TimestampServiceUrl is preferred over the CustomSigner if both are set. If you are using a CustomSigner the delegate method will be passed the raw SHA256 digest of the object to be time stamped (i.e. the document contents). It should return a DER representation of a timestamp token as defined in RFC 3161. The timestamp signing operation is queued so you will typically want to call Doc.Save or Commit after calling this function. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. Also see example code in: XForm AddDocTimestamp Function. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>