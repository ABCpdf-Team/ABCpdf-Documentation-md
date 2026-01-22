# Other Coordinate Spaces

## Basics

ABCpdf uses the standard PDF coordinate space.

The origin of this space is at the bottom left of the document. Distances are measured up and to the right in points.

Windows often uses a top-down coordinate space. The difference between the bottom-up nature of PDF and the top-down nature of Windows can result in confusion. Using the AddGrid method in your code can be very helpful in resolving this type of issue.

Abstracting the coordinate space can make layout easier but removes you from the underlying page layout embedded into your PDF. For this reason we would suggest you stick to the standard PDF coordinate space where practical.

If you wish to use a different coordinate system you can use the document Units and TopDown properties or a Transform to accomplish this. There are subtle differences between these approaches.

## Units

## Transform

Transforms are an inherent part of the PDF specification. They are not an abstraction imposed by ABCpdf but a set of drawing instructions inserted into the PDF document to modify the PDF drawing space. The fact that there is no abstraction can be very useful.

For example suppose you impose a scale transform so you can specify your page layout in mm rather than points. You then call FrameRect and get the raw content stream from the returned object. The coordinates included in the stream are measured in mm rather than points.

However transforms can be difficult to understand and they are extremely literal.

Suppose you impose a transform to flip, scale and translate your coordinate space so that distances are measured in mm from the top left rather than points from the bottom left.

Many graphical objects - lines and rectangles - will appear correctly. However the transform is literal and the flip aspect means that any images and text you add will appear upside down.

