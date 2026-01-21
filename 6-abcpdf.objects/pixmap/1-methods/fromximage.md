---
title: "fromximage"
css: "abcpdf-docs.css"
---

|  |  | FromXImage Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| PixMap static constructor |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp static PixMap FromXImage(ObjectSoup soup, XImage image) ``` [Visual Basic] ``` Shared Function FromXImage(soup As ObjectSoup, image As XImage) As PixMap ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| soup | The ObjectSoup to contain the newly created PixMap. | 
| image | The XImage from which the PixMap should be created. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This method allows you to create a PixMap directly from an XImage object. The PixMap that is created exists within the current Doc.Soup but is not linked into any pages. To link the PixMap into a page it needs to be added as a resource and then drawn from the content stream of the page. |  |  | 
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