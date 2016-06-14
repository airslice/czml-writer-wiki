This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Billboard

A billboard, or viewport-aligned image.  The billboard is positioned in the scene by the `position` property.  A billboard is sometimes called a marker.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the billboard is shown.


**color** - [[Color]]

The color of the billboard.  This color value is multiplied with the values of the billboard's "image" to produce the final color.


**eyeOffset** - [[EyeOffset]]

The eye offset of the billboard, which is the offset in eye coordinates at which to place the billboard relative to the `position` property.  Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis points up, and the Z-axis points into the screen.


**horizontalOrigin** - [[HorizontalOrigin]]

The horizontal origin of the billboard, which determines whether the billboard image is left-, center-, or right-aligned with the `position`.


**image** - [[Uri]]

The URI of the image displayed on the billboard.  For broadest client compatibility, the URI should be accessible via Cross-Origin Resource Sharing (CORS).  The URI may also be a <a href="https://developer.mozilla.org/en/data_URIs">data URI</a>.


**pixelOffset** - [[PixelOffset]]

The offset, in viewport pixels, of the billboard origin from the `position`.  A pixel offset is the number of pixels up and to the right to place the billboard, relative to the `position`.


**scale** - [[Double]]

The scale of the billboard.  The scale is multiplied with the pixel size of the billboard's `image`.  For example, if the scale is 2.0, the billboard will be rendered with twice the number of pixels, in each direction, of the `image`.


**rotation** - [[Double]]

The rotation of the billboard, in radians, counter-clockwise from the alignedAxis.


**alignedAxis** - [[AlignedAxis]]

The aligned axis is the unit vector, in world coordinates, that the billboard up vector points towards.  The default is the zero vector, which means the billboard is aligned to the screen up vector.


**verticalOrigin** - [[VerticalOrigin]]

The vertical origin of the billboard, which determines whether the billboard image is bottom-, center-, or top-aligned with the `position`.


