---
title: "includeall"
css: "abcpdf-docs.css"
---

|  |  | IncludeAll Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default | Read Only | Description | 
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Whether to include all images in the analysis to allow the detection of orphans. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Whether to include all images in the analysis to allow the detection of orphans. By default the ImageOperation will go through the pages defined in the PageContents looking at all the images that are used. However it is possible to include an image in a document yet never use it. This kind of orphan will not be detected using this method. To allow the detection of orphans this property can be used to search the entire document and reference any image that exists. Images that are not referenced on the page will appear in the analysis as an ImageProperties item with no ImageRenditions. However be aware that referenced images may use an unreferenced image as a mask or soft mask so just because an image is not referenced does not necessarily mean it is unused. To detect orphans you need to build a list of unreferenced images and then remove from that any images which appear as the PixMap.Mask or PixMap.SMask of a referenced image. |  |  | 
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