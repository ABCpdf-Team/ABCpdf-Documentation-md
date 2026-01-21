---
title: "transcode"
css: "abcpdf-docs.css"
---

|  |  | Transcode Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Transcodes and reloads the IndirectObject |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp IndirectObject Transcode() ``` [Visual Basic] ``` Function Transcode() As IndirectObject ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| return | An appropriate subclass of IndirectObject. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| PDF objects are not hard typed. The only thing that distinguishes one from another are the named attributes which are applied to them. To enable an appropriate class of IndirectObject to be created ABCpdf has to examine the attributes on the base object and then create an appropriate subclass depending on those characteristics. This is known as transcoding. Normally transcoding takes place automatically as objects are loaded or added. However sometimes changes occur which may result in core aspects of the object changing. These changes may require caches to be regenerated or even an entirely new object to be created - one which better represents the new structure of the object. This is particular the case for the FontObject class as it is heavily dependent on caching and often on other objects in the ObjectSoup. The Transcode method re-interprets this object and if it is appropriate, it returns a newly created object of an appropriate subclass. If transcoding results in a new object being created it will displace the current object from the soup. As such you will need to discard the old object if a new one is returned. |  |  | 
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