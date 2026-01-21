---
title: "6-whatsnew"
css: "abcpdf-docs.css"
---

# What's New?

## Linux Support

ABCpdf now runs on Linux as well as Windows. Great for cross platform deployments!

In almost all cases your code will run in the same way on both platforms. There are a few differences but these are small and obscure and generally relate to Windows specific features like XPS and WPF.

For details see our [ABCpdf on Linux](../2-getting_started/6-platforms.md) pages.

## ABCChrome

The HTML engines have been upgraded. Along with the older engines we now support ABCChrome 123 and 117.

This new engine features better conformance, new features and higher security.

Perhaps most importantly, conversion speeds are substantially higher than previous versions.

Our local HTML conversion tasks typically finish in half the time. Yes twice as fast!

## ABCWebKit

The ABCWebKit engine is unique in that it is so self contained and operates so easily on minimalist operating systems.

However it is old and lacks security which means that FireShield is vital if you want to use it.

In this release FireShield runs ABCWebKit in a Windows Job Object for added control and diagnostic information.

After each conversion we provide statistics like the number of bytes transferred over the network, the number of bytes read, the number written, the amount of user and kernel time taken, peak memory, amongst others.

## FireShield

We have always been big on security and FireShield has been at the heart of this for HTML conversion. FireShield allows us to run our HTML engines inside a customized sandbox.

In the new release FireShield has been significantly extended to ensure greater control over file and directory access. The way you specify paths has been simplified and the level of lockdown extended.

In the past the FireShield sandbox has been primarily based around dynamic file permissions.

In this release we extend it to network access so that you can lock down your application both in terms of file paths and also IP address.

FireShield now includes rewrite rules to allow file access to be redirected from one area to another. So, for example, you can change the temp directory on the fly to isolate each conversion.

## Pentest

As in previous releases our regular third party penetration testing feeds into new features and enhanced security.

This is not something that is very visible but it is ever present. We take security seriously and every little helps.

## Images

We used to support JPEG 2000 export in only eight and sixteen bit color depth. To this we add one, two and three bit, also embedded ICC profiles and resolution information.

Previously the JPEG 2000 decode process had been single threaded which means that there was a bottleneck if you were processing multiple images at the same time. In this release the code is thread safe which means multiple image decompression is much faster.

The XImage object allows you to load images prior to drawing onto a document page. It has always provided standard information such as width, height and resolution. However the concept of standard tends to mean lowest common denominator, which means that format specific information is not available.

In this release we allow you to get format specific information using the new XImage.GetInfo method.

The JPEG 2000 format implements a "Structure" info which provides the tag structure of the raw data together with types, offsets and lengths. This can be used to modify or insert tags for custom output.

The TIFF format implements a "TiffTag:" info which allows you to get the values of TIFF tags either by name or number. Simply append the item you are interested in. For example you might use "TiffTag:InkNames" to get the ink or "TiffTag:271" to retrieve the scanner manufacturer.

We have been bumping up against the capabilities of Windows for some time when it comes to image import. In this release we include our own custom PNG, GIF, JPEG and BMP codecs accessible via ReadModule.Png, ReadModule.Gif, ReadModule.Jpeg and ReadModule.Bmp.

Our PNG import module supports all PNG bit depths (1, 8, 16) and color spaces (grayscale and RGB) in the PNG specification and allows import preserving those native depths and color spaces.

Our BMP export module supports alpha (SaveAlpha), embedded color profiles (IccOutput), indexed color in various bit depths (ColorSpace & Palette) in both compressed and non-compressed formats (SaveCompression).

## Cloud Vision

The CloudVisionOperation allows access to google cloud vision APIs in a simple and integrated manner.

We have found this API to be extremely good for the OCR of text. Our reading order algorithms are better once the text has been recognized so we do not extend into the structure analysis which google provides.

Other options allows you to automatically tag images with sensible descriptions - extremely useful when creating accessible PDFs.

## Rendering

We now support rendering filters for selective rendering. So if you want to render a PDF without text or without color or without paths then this is now a trivial thing to do.

To use this feature set the XRendering.OpsToIgnore property to select operators which should be ignored.

## Signatures

The Signature class has been extensively enhanced to allow more sophisticated control over the signing process.

- You can control the revocation policy used when querying the status of a signature for Long Term Validation (LTV).
- There is a simpler and more logical algorithm for determining the length of signatures produced using external delegates.
- There are more flexible options for specifying the type of data that an external signing delegate will accept and produce.
- There are more flexible options for creating document-wide Certification signatures.
- The XSettings.Log property provides a verbose description of the stages of document signing.

This release includes functionality to allow you to extract individual revisions from a multi-revision PDF. Simply use the ObjectSoup.RevisionEOFs property to determine the end of the revision and then truncate the file to that location.

## Operations

The ImageOperation has been highly optimized to allow fast access to image properties. In our tests it comes in four or five times faster.

The ReduceSizeOperation has been improved to further allow the size of PDFs to be reduced. Some changes are internal and some are switchable using properties like RemoveUnusedImages and RemoveUnusedFonts.

There is a new Accessibility operation to allow access to and manipulation of the document tagging structure for Accessible PDF documents.

## Contents &amp; Streams

The Page object now contains GetContentData and SetContentData for easy and efficient access to the page content stream.

The StreamObject class now includes overrides for GetData for simple and efficient extraction of data without affecting the underlying compression options. It includes new overloads for SetData to allow simpler and more efficient assignment of data to an existing stream.

The ContentStreamOperation has been extensively enhanced to allow you to determine the position of operators in the underlying streams and enable the underlying data to be tweaked or adjusted. The GetPositionAndLength and GetStreamAndOffset methods allows easy access to the offsets of a particular operator.

There are new properties to allow Annotations to be handled more easily and methods to allow operation on individual layers of a page or individual Form XObjects.

## Examples

The changes in ABCpdf have allowed significant simplification of a number of example projects.

Most notably the AccessiblePDF project is much more self contained as much of the required accessibility functionality is now contained in the Accessibility operation.

## Other

And as usual there's a whole host of useful new functions and properties like:

- ArrayAtom.ItemsPerLine - allows you to specify different numbers of items per line.
- ArrayAtom.ToString format specifiers - "n" allows you to specify items per line (eg n10).
- ArrayAtom.IsContentStream - determines if the array can hold operators and streams.
- NumAtom(long) constructor - for easy construction of large NumAtoms.
- NumAtom.IsInt - allows you to determine if a NumAtom is integer or real.
- ValidAsInt32 - whether the value is valid as a 32 bit integer.
- ValidAsInt64 - whether the value is valid as a 64 bit integer.
- XSettings.SetConfigFile - allows you to specify a Linux style config file.
- TextStyle.Pilcrows - allows you to display pilcrows when you add text.
- FontObject.VetText - allows you to vet text to ensure it is compatible with a particular encoding.
- SVG import now allows the use of grayscale and CMYK colors.