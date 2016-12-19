This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Rectangle

A cartographic rectangle, which conforms to the curvature of the globe and can be placed on the surface or at altitude and can optionally be extruded into a volume.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the rectangle is shown.

Default: `true`


**coordinates** - [[RectangleCoordinates]]

The coordinates of the rectangle.


**height** - [[Double]]

The height of the rectangle.


**extrudedHeight** - [[Double]]

The extruded height of the rectangle.


**rotation** - [[Double]]

The rotation of the rectangle clockwise from north.


**stRotation** - [[Double]]

The rotation of any applied texture. A positive rotation is counter-clockwise.


**granularity** - [[Double]]

The sampling distance, in radians.


**fill** - [[Boolean]]

Whether or not the rectangle is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the rectangle.


**outline** - [[Boolean]]

Whether or not the rectangle is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the rectangle outline.


**outlineWidth** - [[Double]]

The width of the rectangle outline.

Default: `1.0`


**closeTop** - [[Boolean]]

Whether to close the top of the rectangle.

Default: `true`


**closeBottom** - [[Boolean]]

Whether to close the bottom of the rectangle.

Default: `true`


**shadows** - [[ShadowMode]]

Whether or not the rectangle casts or receives shadows.

Default: `DISABLED`


