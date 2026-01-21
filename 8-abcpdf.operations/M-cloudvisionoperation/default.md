---
title: "default"
css: "abcpdf-docs.css"
---

# CloudVisionOperation Class

Google Cloud Vision API utilities.

These can be used for:.

- Optical Character Recognition (OCR) on raster or vector documents.
- Automatically tagging embedded images with meaningful descriptions.

This class requires .NET 5 or later.
            ``` System.Object WebSupergoo.ABCpdf13.Operations.CloudVisionOperation ```

## Method Description CloudVisionOperation Create a CloudVisionOperation. AddPages Add all the pages of the document for processing. AddPage Add one page of the document for processing. StartOcr Start OCR operation on the pages that have been added. TagImages Start image tagging operation on the pages that have been added. WaitAll Wait until the operation is completed. &nbsp;

## Property Description S&raquo;&nbsp;Client The HttpClient instance to use for making web requests. AddWords Whether to OCR and add the text of detected words to the processed pages. WordColor Whether to make detected words visible using a particular color. ParaColor Whether to outline paragraphs using a particular color. BlockColor Whether to outline blocks using a particular color. ConfidenceColor The confidence color indicating the reliability of the OCR for each piece of text. Flatten Whether to flatten the page after text is added. ApiKey The Google API key to use for requests. RetryCount The number of times to retry if the service is not available. Dpi The DPI of the page. AngleRounding In the case that text is drawn at an angle, this property allows a snap-to-fit effect. MinimumSize The minimum size of image which should be passed to OCR. MaximumSize The maximum size of image which should be passed to OCR. CloudVisionTask The task associated with the current request. ProgressNow The number of operation tasks which have been completed. ProgressMax The total number of operation tasks to be completed.