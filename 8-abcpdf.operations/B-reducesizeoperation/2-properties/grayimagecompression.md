# GrayImageCompression       Property

| **Type** | **Default** | **Read Only** | **Description** |
| --- | --- | --- | --- |
|  | Jpeg | No | The target compression type for the re-encoding of grayscale images. |

## Notes

The target compression type for the re-encoding of grayscale images.

When the [CompressImages](compressimages.md) setting is used this option is used to determine the type of compression to be used for images in this color space. Images are recompressed if they are resampled or if the target compression type is lossy. They are not recompressed if they already use the target compression and the compression type is lossless.

## Example

None
