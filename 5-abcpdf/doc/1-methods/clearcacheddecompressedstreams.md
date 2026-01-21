---
title: "clearcacheddecompressedstreams"
css: "abcpdf-docs.css"
---

|  |  | ClearCachedDecompressedStreams Function |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Clears the cached, decompressed data for stream objects. |  |  | 

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Syntax</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| **[C#]** ```csharp void ClearCachedDecompressedStreams() void ClearCachedDecompressedStreams(StreamObjectTypes types) ``` [Visual Basic] ``` Sub ClearCachedDecompressedStreams() Sub ClearCachedDecompressedStreams(types As StreamObjectTypes) ``` |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Params</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Name | Description | 
| --- | --- |
| types | The types of stream objects whose cached, decompressed data are discarded. The default value is All. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| Use this method to discards the cached, decompressed data for multiple stream objects. The StreamObjectTypes enumeration may take a combination of the following values: None – no stream object. All – all stream objects. Others – stream objects not of the below types. PixMap FormXObject – Form XObject. TilingPattern – tiling pattern object. StreamShadingObject – shading objects that are streams. StreamFunction – function objects that are streams. You can apply the effect to a single stream object using StreamObject.ClearCachedDecompressed. |  |  | 
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