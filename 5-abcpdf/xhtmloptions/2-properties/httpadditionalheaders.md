---
title: "httpadditionalheaders"
css: "abcpdf-docs.css"
---

|  |  | HttpAdditionalHeaders Property |  |  | 
| --- | --- | --- | --- | --- |
|  |  |  | 
| Type | Default Value | Read Only | Description | 
| **[C#]** ```csharp string ``` [Visual Basic]`String` | "" | No | Additional HTTP headers to send in the request. | 

</TD>
          <TD width=60>&nbsp;</TD>
          <TD>&nbsp;</TD></TR></TBODY></TABLE></TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Notes</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| This property specifies HTTP headers added to the default headers. It must follow the syntax of HTTP headers, typically delimited using a cr+lf combination. For example, you may add the cookies from a response to a request under some authentication (e.g. ASP.NET Forms) where a session ID is returned for subsequent requests so re-authentication is not needed. See the NoCookie property for further information if you specify cookies in the HTTP headers. The headers are sent only in the request for the URL; they are not sent in the requests for the linked resources (e.g. CSS and images) in the obtained HTML page. The additional headers are always used by the MSHTML Engine. Under Gecko, these headers are only sent if you are using the Screen Media or if you are using the POST RequestMethod. When this occurs, ABCpdf needs to obtain and store a local copy of the web page before invoking the engine. This property is not valid under ABCChrome. |  |  | 
| --- | --- | --- |

</TD></TR>
  <TR>
    <TD class=sectheader vAlign=top>![](../../../images/steel-pin.gif)  
Example</TD>
    <TD width=14>&nbsp;</TD>
    <TD vAlign=top>
      
| The following example shows how this property may be used. [C#] ```csharp using var doc = new Doc(); string url = "https://www.websupergoo.com/"; // assign appropriate URL var request = (HttpWebRequest)WebRequest.Create(url); request.CookieContainer = new CookieContainer(); // required for HttpWebResponse.Cookies request.Credentials = null; // assign appropriate credentials using (var resp = request.GetResponse()) { // cookieless Forms Authentication adds authentication ticket to the URL url = resp.ResponseUri.AbsoluteUri; var response = (HttpWebResponse)resp; if (response.Cookies.Count > 0) { // includes ASP.NET_SessionId bool needsCookie2 = false; var builder = new StringBuilder("Cookie: "); for (int i = 0; i 0) builder.Append("; "); builder.Append(cookie.ToString()); } builder.Append(!needsCookie2 ? "\r\n" : "\r\nCookie2: $Version=1\r\n"); doc.HtmlOptions.HttpAdditionalHeaders = builder.ToString(); } } doc.HtmlOptions.Engine = EngineType.MSHtml; doc.HtmlOptions.NoCookie = true; doc.HtmlOptions.PageLoadMethod = PageLoadMethodType.MonikerForHtml; int id = doc.AddImageUrl(url); doc.Save(Server.MapPath("HttpHeaders.pdf")); ``` [Visual Basic] ```vbnet Using doc As New Doc() Dim url As String = "https://www.websupergoo.com/" ' assign appropriate URL Dim request As HttpWebRequest = DirectCast(WebRequest.Create(url), HttpWebRequest) request.CookieContainer = New CookieContainer() ' required for HttpWebResponse.Cookies request.Credentials = Nothing ' assign appropriate credentials Using resp As WebResponse = request.GetResponse() ' cookieless Forms Authentication adds authentication ticket to the URL url = resp.ResponseUri.AbsoluteUri Dim response As HttpWebResponse = DirectCast(resp, HttpWebResponse) If response.Cookies.Count > 0 Then ' includes ASP.NET_SessionId Dim needsCookie2 As Boolean = False Dim builder As New StringBuilder("Cookie: ") Dim i As Integer = 0 While i 1 Then needsCookie2 = True End If If i > 0 Then builder.Append("; ") End If builder.Append(cookie.ToString()) System.Threading.Interlocked.Increment(i) End While builder.Append(If(Not needsCookie2, vbCr & vbLf, vbCr & vbLf & "Cookie2: $Version=1" & vbCr & vbLf)) doc.HtmlOptions.HttpAdditionalHeaders = builder.ToString() End If End Using doc.HtmlOptions.Engine = EngineType.MSHtml doc.HtmlOptions.NoCookie = True doc.HtmlOptions.PageLoadMethod = PageLoadMethodType.MonikerForHtml Dim id As Integer = doc.AddImageUrl(url) doc.Save(Server.MapPath("HttpHeaders.pdf")) End Using ``` ASP.NET_SessionId. If your application runs in ASP.NET, you cannot use the cookie from the application's originating request as it identifies the session. If the site containing the target HTML page is different from your site, the session ID is invalid. If it is the same, this will cause a re-entrance in the same session, and ASP.NET may not allow re-entrance for the same session. | 
| --- |

</TD>
          <TD width=60>&nbsp;</TD>
          <TD width=11>&nbsp;</TD></TR></TBODY></TABLE></TD></TR></TBODY></TABLE>