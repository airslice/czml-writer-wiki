This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Label

A string of text.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the label is shown.

Default: `true`


**text** - [[String]]

The text displayed by the label.  The newline character (\n) indicates line breaks.


**font** - [[Font]]

The font to use for the label.


**style** - [[LabelStyle]]

The style of the label.


**scale** - [[Double]]

The scale of the label.  The scale is multiplied with the pixel size of the label's text.  For example, if the scale is 2.0, the label will be rendered with twice the number of pixels, in each direction, of the text.

Default: `1.0`


**showBackground** - [[Boolean]]

Whether or not a background behind the label is shown.

Default: `false`


**backgroundColor** - [[Color]]

The color of the background behind the label.


**backgroundPadding** - [[BackgroundPadding]]

The amount of padding between the text and the label's background.


**pixelOffset** - [[PixelOffset]]

The offset, in viewport pixels, of the label origin from the `position`.  A pixel offset is the number of pixels up and to the right to place the label, relative to the `position`.


**eyeOffset** - [[EyeOffset]]

The eye offset of the label, which is the offset in eye coordinates at which to place the label relative to the `position` property.  Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis points up, and the Z-axis points into the screen.


**horizontalOrigin** - [[HorizontalOrigin]]

The horizontal origin of the label.  It controls whether the label is left-, center-, or right-aligned with the `position`.

Default: `CENTER`


**verticalOrigin** - [[VerticalOrigin]]

The vertical origin of the label.  It controls whether the label image is bottom-, center-, or top-aligned with the `position`.

Default: `CENTER`


**heightReference** - [[HeightReference]]

The height reference of the label, which indicates if the position is relative to terrain or not.

Default: `NONE`


**fillColor** - [[Color]]

The fill color of the label.


**outlineColor** - [[Color]]

The outline color of the label.


**outlineWidth** - [[Double]]

The outline width of the label.

Default: `1.0`


**translucencyByDistance** - [[NearFarScalar]]

How the label's translucency should change based on the label's distance from the camera.  This scalar value should range from 0 to 1.


**pixelOffsetScaleByDistance** - [[NearFarScalar]]

How the label's pixel offset should change based on the label's distance from the camera.  This scalar value will be multiplied by `pixelOffset`.


