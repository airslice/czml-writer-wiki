This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Label

A string of text.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the label is shown.


**eyeOffset** - [[EyeOffset]]

The eye offset of the label, which is the offset in eye coordinates at which to place the label relative to the `position` property.  Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis points up, and the Z-axis points into the screen.


**fillColor** - [[Color]]

The fill color of the label.


**font** - [[Font]]

The font to use for the label.


**horizontalOrigin** - [[HorizontalOrigin]]

The horizontal origin of the label.  It controls whether the label is left-, center-, or right-aligned with the `position`.


**outlineColor** - [[Color]]

The outline color of the label.


**outlineWidth** - [[Double]]

The outline width of the label.


**pixelOffset** - [[PixelOffset]]

The offset, in viewport pixels, of the label origin from the `position`.  A pixel offset is the number of pixels up and to the right to place the label, relative to the `position`.


**scale** - [[Double]]

The scale of the label.  The scale is multiplied with the pixel size of the label's text.  For example, if the scale is 2.0, the label will be rendered with twice the number of pixels, in each direction, of the text.


**style** - [[LabelStyle]]

The style of the label.


**text** - [[String]]

The text displayed by the label.


**verticalOrigin** - [[VerticalOrigin]]

The vertical origin of the label.  It controls whether the label image is bottom-, center-, or top-aligned with the `position`.


