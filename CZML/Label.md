This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Label

A string of text.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the label is shown.

Default: `true`


**text** - [[String]]

The text displayed by the label. The newline character (\n) indicates line breaks.


**font** - [[Font]]

The font to use for the label.

Default: `30px sans-serif`


**style** - [[LabelStyle]]

The style of the label.

Default: `FILL`


**scale** - [[Double]]

The scale of the label. The scale is multiplied with the pixel size of the label's text. For example, if the scale is 2.0, the label will be rendered with twice the number of pixels, in each direction, of the text.

Default: `1.0`


**showBackground** - [[Boolean]]

Whether or not a background behind the label is shown.

Default: `false`


**backgroundColor** - [[Color]]

The color of the background behind the label.

Default: `[0.165, 0.165, 0.165, 0.8]`


**backgroundPadding** - [[BackgroundPadding]]

The amount of padding between the text and the label's background.

Default: `[7, 5]`


**pixelOffset** - [[PixelOffset]]

The offset, in viewport pixels, of the label origin from the `position`. A pixel offset is the number of pixels up and to the right to place the label, relative to the `position`.

Default: `[0.0, 0.0]`


**eyeOffset** - [[EyeOffset]]

The eye offset of the label, which is the offset in eye coordinates at which to place the label relative to the `position` property. Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis points up, and the Z-axis points into the screen.

Default: `[0.0, 0.0, 0.0]`


**horizontalOrigin** - [[HorizontalOrigin]]

The horizontal origin of the label. It controls whether the label is left-, center-, or right-aligned with the `position`.

Default: `CENTER`


**verticalOrigin** - [[VerticalOrigin]]

The vertical origin of the label. It controls whether the label image is bottom-, center-, or top-aligned with the `position`.

Default: `CENTER`


**heightReference** - [[HeightReference]]

The height reference of the label, which indicates if the position is relative to terrain or not.

Default: `NONE`


**fillColor** - [[Color]]

The fill color of the label.

Default: `white`


**outlineColor** - [[Color]]

The outline color of the label.

Default: `black`


**outlineWidth** - [[Double]]

The outline width of the label.

Default: `1.0`


**translucencyByDistance** - [[NearFarScalar]]

How the label's translucency should change based on the label's distance from the camera. This scalar value should range from 0 to 1.


**pixelOffsetScaleByDistance** - [[NearFarScalar]]

How the label's pixel offset should change based on the label's distance from the camera. This scalar value will be multiplied by `pixelOffset`.


**scaleByDistance** - [[NearFarScalar]]

How the label's scale should change based on the label's distance from the camera. This scalar value will be multiplied by `scale`.


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this label will be displayed.


**disableDepthTestDistance** - [[Double]]

The distance from the camera at which to disable the depth test. This can be used to prevent clipping against terrain, for example. When set to zero, the depth test is always applied. When set to Infinity, the depth test is never applied.

Default: `0.0`


