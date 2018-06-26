This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Rectangle

A cartographic rectangle, which conforms to the curvature of the globe and can be placed on the surface or at altitude and can optionally be extruded into a volume.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the rectangle is shown.

Default: `true`


**coordinates** - [[RectangleCoordinates]] - **Required**

The coordinates of the rectangle.


**height** - [[Double]]

The height of the rectangle.

Default: `0.0`


**extrudedHeight** - [[Double]]

The extruded height of the rectangle.


**rotation** - [[Double]]

The rotation of the rectangle clockwise from north.

Default: `0.0`


**stRotation** - [[Double]]

The rotation of any applied texture. A positive rotation is counter-clockwise.

Default: `0.0`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**fill** - [[Boolean]]

Whether or not the rectangle is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the rectangle.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the rectangle is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the rectangle outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the rectangle outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the rectangle casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying at what distance from the camera this rectangle will be displayed.


**zIndex** - [[Integer]]

The z-index of the rectangle, used for ordering ground geometry. Only has an effect if the rectangle is constant, and `height` and `extrudedHeight` are not specified.

Default: `0`


