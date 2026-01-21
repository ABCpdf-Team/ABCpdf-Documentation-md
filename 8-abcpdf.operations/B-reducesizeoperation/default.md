---
title: "default"
css: "abcpdf-docs.css"
---

# ReduceSizeOperation Class

Operation to reduce the size of a document.

The default settings here are aimed a reasonably aggressive size reduction. The most common changes you may wish to make relate to monochrome (eg black and white) images and palettization. The default settings here may be too aggressive for some applications so may require a little moderation. See the [MonochromeImageDpi](2-properties/monochromeimagedpi.md) property for details.

``` System.Object WebSupergoo.ABCpdf13.Operations.Operation WebSupergoo.ABCpdf13.Operations.ReduceSizeOperation ```

## Method Description &nbsp;ReduceSizeOperation ReduceSizeOperation Constructor. &nbsp;Compact Compact and compress the document. &nbsp;

## Property Description CompressImages Whether to resize and recompress images where possible. CompressStreams Whether to compress uncompressed streams where possible. ColorImageCompression The target compression type for the re-encoding of color images. ColorImageDpi The target resolution for the resampling of color images. ColorImageQuality The target compression quality for the re-encoding of color images. GrayImageCompression The target compression type for the re-encoding of grayscale images. GrayImageDpi The target resolution for the resampling of grayscale images. GrayImageQuality The target compression quality for the re-encoding of grayscale images. MonochromeImageCompression The target compression type for the re-encoding of monochrome images. MonochromeImageDpi The target resolution for the resampling of monochrome images. MonochromeImageQuality The target compression quality for the re-encoding of monochrome images. PageContents The pages to be operated upon. PalettizationTolerance The amount of divergence from the target palette which will be allowed. RefactorImages Whether to refactor and remove duplicate images where possible. RemoveUnusedFonts Whether to refactor and remove unused fonts where possible. RemoveUnusedImages Whether to refactor and remove unused images where possible. UnembedComplexFonts Whether to unembed complex Unicode based fonts where possible. UnembedCorruptFonts Whether to unembed embedded fonts that appear to be corrupt or non-standard. UnembedSimpleFonts Whether to unembed simple Latin based fonts where possible. UnembedUnusualFonts Whether to unembed embedded fonts that do not have an obvious substitute on the local machine.