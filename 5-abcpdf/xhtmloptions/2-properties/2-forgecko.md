---
title: "2-forgecko"
css: "abcpdf-docs.css"
---

|  |  | ForGecko Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp IHtmlGeckoOptions ``` [Visual Basic] `IHtmlGeckoOptions` | n/a | Yes | An object that provides access to only the HTML options supported by the Gecko HTML engine. | 

</td>
          <td width="60">&nbsp;</td>
          <td>&nbsp;</td></tr></tbody></table></td></tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Notes</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| The HTML options supported by the ABCGecko HTML engine. ### Supported methods GetGeckoVersion — also initializes the Gecko engine. EndTasks GetHttpStatusCode GetScriptReturn GetTagIDs GetTagRects GetTagUntransformedRects LinkDestinations LinkPages ### Supported properties AddForms AddLinks AddMovies (Flash only) AddTags BrowserWidth ContentCount FontEmbed FontSubset FontSubstitute FontProtection HideBackground ImageQuality ImprovePageBreakAvoid ImprovePageBreakInTable InitialWidth LogonName LogonPassword MakeFieldNamesUnique Media NoDefaultBackground NoSnapRounding OnLoadScript ProcessOptions RequestMethod RetryCount Timeout UseNoCache UseScript The HttpAdditionalHeaders property is supported under some circumstances but because these are unusual it is not included in this interface. For details see the documentation for this property. |  |  | 
| --- | --- | --- |

</td></tr>
  <tr>
    <td class="sectheader" valign="top">![](../../../images/steel-pin.gif)  
Example</td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| [C#] ```csharp using var doc = new Doc(); doc.HtmlOptions.Engine = EngineType.Gecko; doc.HtmlOptions.ForGecko.AddLinks = true; // You can store a reference to the filter to reduce code repetition var options = doc.HtmlOptions.ForGecko; options.AddLinks = true; doc.AddImageUrl("http://www.websupergoo.com"); doc.Save(Server.MapPath("wsg2.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() doc.HtmlOptions.Engine = EngineType.Gecko doc.HtmlOptions.ForGecko.AddLinks = True ' You can store a reference to the filter to reduce code repetition Dim options As IHtmlGeckoOptions = doc.HtmlOptions.ForGecko options.AddLinks = True doc.AddImageUrl("http://www.websupergoo.com") doc.Save(Server.MapPath("wsg2.pdf")) End Using ``` |  |  | 
| --- | --- | --- |

</td></tr></tbody></table>