---
title: "default"
css: "abcpdf-docs.css"
---

|  |  | XHtmlOptions Object |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Represents the current HTML rendering settings. The properties of this object may be used to control the way that the Doc.AddImageUrl and Doc.AddImageHtml methods work. The methods of this object operate on objects added using the the Doc.AddImageUrl and Doc.AddImageHtml methods. Some operations change the document. Others provide information about the content which has been added. HTML documents can be imported using different HTML engines. The current supported ones are the MSHTML engine (used in Microsoft Internet Explorer) and a modified version of Mozilla Firefox's Gecko engine tailored to work with ABCpdf. Different engines interpret HTML documents in different ways and support a different set of HTML options, please see the Engine property for details. ``` System.Object WebSupergoo.ABCpdf13.XHtmlOptions ``` |  |  | 

</td></tr>
  <tr>
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| Method | Description | 
| --- | --- |
| EndTasks | Ends any HTML Engine worker threads or processes. | 
| GetHttpStatusCode | Retrieves the HTTP status code. | 
| GetScriptReturn | Retrieves the client side onload script return value. | 
| GetTagIDs | Gets an array of the HTML IDs of tagged visible items. | 
| GetTagRects | Gets an array of the locations of tagged visible items. | 
| GetTagUntransformedRects | Gets an array of the locations of tagged visible items before Doc.Transform is applied. | 
| LinkDestinations | Convert a restricted selection of external links to internal links. | 
| LinkPages | Convert external links to internal links wherever possible. | 
| PageCacheClear | Clears the HTML page cache. | 
| PageCachePurge | Purges the HTML page cache. | 
| SetTheme | Specify whether to use Windows themes or not. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td></tr></tbody></table></td></tr>
  <tr>
    <td valign="top">&nbsp; </td>
    <td width="14">&nbsp;</td>
    <td valign="top">
      
| Property | Description | 
| --- | --- |
| Engine | The engine to use for HTML import operations. | 
| ForChrome | An object that provides access to only the HTML options supported by the ABCChrome engine. | 
| ForMSHtml | An object that provides access to only the HTML options supported by the MSHTML engine. | 
| ForGecko | An object that provides access to only the HTML options supported by the ABCGecko HTML engine. | 
| ForWebKit | An object that provides access to only the HTML options supported by the ABCWebKit engine. | 
| AddForms | Whether form fields should be live. | 
| AddLinks | Whether hyperlinks should be live. | 
| AddMovies | Whether active content such as movies should be added. | 
| AddTags | Whether location of certain tags should be noted. | 
| AddIDs | Whether HTML ID attributes should be tracked. | 
| AddNames | Whether HTML name attributes should be tracked. | 
| AdjustLayout | Whether HTML layout is checked and adjusted for optimal output to PDF. | 
| AutoTruncate | Whether to automatically clip redundant content at the end of the page. | 
| BaseURI | The base URL to use for all relative URLs in the page. | 
| BreakMethod | The page break logic for HTML. | 
| BreakZoneSize | The percentage of the current drawing area in which HTML breaks can occur. | 
| BrowserWidth | The width of the virtual browser in pixels. | 
| CoerceVector | The conditions under which to coerce a vector output. | 
| CommandOptions | A set of command options for the HTML engine. | 
| ContentCount | The minimum number of content items required for a page to be valid. | 
| DeactivateWebBrowser | Whether to deactivate the WebBrowser. | 
| DisableVectorCoercion | The conditions under which to disable vector-output coercion. | 
| DoMarkup | Whether HTML pages are marked up before conversion to PDF. | 
| FireShield | The FireShield™ security settings to be applied to the ABCChrome engine. | 
| FontEmbed | Whether fonts should be embedded rather than referenced. | 
| FontProtection | Whether fonts should be protected. | 
| FontSubset | Whether embedded fonts should be subsetted or not. | 
| FontSubstitute | Whether font substitution should be used to reduce file size. | 
| HideBackground | Whether to hide the background color of a page. | 
| HostWebBrowser | Whether to host a WebBrowser control. | 
| HtmlCallback | The multicast delegate to be called while HTML rendering is taking place. | 
| HtmlEmbedCallback | The multicast delegate to be called when embedding an object while HTML rendering is taking place. | 
| HttpAdditionalHeaders | Additional HTTP headers to send in the request. | 
| IgnoreCertificateErrors | Whether to ignore certificate-related errors. | 
| ImageQuality | The quality of compression acceptable for continuous tone images such as JPEGs. | 
| ImprovePageBreakAvoid | Whether to improve the support for page-break-inside of avoid. | 
| ImprovePageBreakInTable | Whether to improve the support for page break in table to prevent missing rows. | 
| InitialWidth | The minimum width to be used for auto-sized pages. | 
| LogonName | A user name to be used for authentication. | 
| LogonPassword | A password to be used for authentication. | 
| MakeFieldNamesUnique | Whether field names should be changed to make them unique. | 
| MaxAtomicImageSize | The maximum size at which an image may be regarded as unbreakable. | 
| Media | The CSS media type to use. | 
| NoCookie | Whether to disable automatic cookies. | 
| NoDefaultBackground | Whether to disable the default background color. | 
| NoSnapRounding | Whether to disable the snap rounding of coordinates and lengths. | 
| NoTheme | Whether themes should be disabled. | 
| OnLoadScript | A script to be run after the page is loaded. | 
| PageCacheEnabled | Whether the page cache should be searched before rendering the page. | 
| PageCacheExpiry | The length of time that pages can be held in the cache (ms). | 
| PageCacheSize | The number of pages that can be held in the cache. | 
| Paged | Whether content should be rendered in multipaged format. | 
| PageLoadMethod | The method for loading URI/HTML. | 
| ProcessOptions | The options for new worker processes. | 
| ReloadPage | Whether to reload page. | 
| RepaintDelay | Minimum time to wait for the page to finish animation (ms). | 
| RepaintTimeout | Maximum time to wait for the page to finish animation (ms). | 
| RequestMethod | The request method for URL. | 
| RetryCount | The number of times a page should be retried if unavailable or invalid. | 
| TargetLinks | Whether hyperlinks should be allowed to open new windows. | 
| Timeout | The maximum amount of time allowed for obtaining a page (ms). | 
| TransferModule | The module for obtaining URI/HTML data. | 
| UseActiveX | Whether to enable ActiveX. | 
| UseJava | Whether to enable Java. | 
| UseNoCache | Whether any proxy servers should re-request items of content. | 
| UserAgent | The user-agent string. | 
| UseResync | Whether to resynchronize pages. | 
| UseProxyServer | Whether to use a proxy server. | 
| UseScript | Whether to enable JavaScript and VBScript. | 
| UseTheme | Whether to use themes. | 
| UseVideo | Whether to enable Video. | 

</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td></tr>
        <tr>
          <td>&nbsp;</td>
          <td width="60">&nbsp;</td>
          <td width="11">&nbsp;</td></tr></tbody></table></td></tr></tbody></table>