---
title: "06-clearcache"
css: "abcpdf-docs.css"
---

|  |  | ClearCache Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Clears any cached Element items. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp virtual void ClearCache() ``` [Visual Basic] ``` Overridable Function ClearCache() As void ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| none |  | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Clears any cached Element items. Elements in properties are cached so that the Element you assign to a property is the same as the one you retrieve when you later get that property. However it is possible that sometimes this behavior is not what you want. For example suppose you assign a DeviceColorSpaceElement to a property and then later change the underlying Atom so that it is really a CalRGBColorSpace. In this situation the retrieved ColorSpaceElement will continue to be interpreted as a DeviceColorSpaceElement and an invalid one at that. What you really want to do here is to clear the cached Element thus allowing the property to be regenerated as a CalRGBColorSpace. This function clears the cached Elements to allow this to happen. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| None. |  |  | 
| --- | --- | --- |

</TD></TR></TBODY></TABLE>