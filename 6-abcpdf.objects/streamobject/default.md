---
title: "default"
css: "abcpdf-docs.css"
---

# StreamObject Class

A PDF data stream.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.StreamObject WebSupergoo.ABCpdf13.Objects.D3DStream WebSupergoo.ABCpdf13.Objects.EmbeddedFile WebSupergoo.ABCpdf13.Objects.FormXObject WebSupergoo.ABCpdf13.Objects.IccProfile WebSupergoo.ABCpdf13.Objects.Layer WebSupergoo.ABCpdf13.Objects.PixMap ```

## Method Description &nbsp;StreamObject StreamObject Constructor. ClearData Clear the data and compression settings for the stream. ClearCachedDecompressed Clear the cached, decompressed data for the stream. Compress Compress the data in the stream. CompressAscii85 Compress the data in the stream using ASCII 85 encoding. CompressAsciiHex Compress the data in the stream using the ASCII Hex encoding. CompressFlate Compress the data in the stream using Flate compression. CompressRunLength Compress the data in the stream using run length encoding. CopyDecompressedData Copy the decompressed binary content of the stream into a byte array. Decompress Decompress the data in the stream. GetData Get the raw binary content of the stream. GetText Get the content of the stream as a string. SetData Set the raw binary content of the stream. &nbsp;SetFile Set the raw binary content of the stream using data from a file. SetText Set the content of the stream as a string. inherited methods... &nbsp;

## Property Description Compressed Whether the stream data is compressed or otherwise encoded. Compression The primary compression type. Compressions All the compression types applied to the stream. Length The number of bytes of encoded stream data. inherited properties...