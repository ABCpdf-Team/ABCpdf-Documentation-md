# WebPageOperation Class

Web page operation used to import HTML or URLs into a complete multi-page document enabling document tagging for accessibility.

Only the ABCChrome engines support this functionality. Later versions of ABCChrome are much superior to earlier ones.

``` System.Object WebSupergoo.ABCpdf13.Operations.WebPageOperation ```

## Method Description WebPageOperation Create a WebPageOperation. ReadHtml Read a string of HTML into a paged PDF document. ReadUrl Read a URL into a paged PDF document. &nbsp;

## Property Description Doc The Doc object on which to operate. Tagged Whether the document should be tagged for accessibility. Outline Whether the document should contain a document outline based on the HTML content. HeaderHtml Any HTML header required for the page. FooterHtml Any HTML footer required for the page.