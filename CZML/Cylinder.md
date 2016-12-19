This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Cylinder

A cylinder, truncated cone, or cone defined by a length, top radius, and bottom radius.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the cylinder is shown.

Default: `true`


**length** - [[Double]]

The length of the cylinder.


**topRadius** - [[Double]]

The radius of the top of the cylinder.


**bottomRadius** - [[Double]]

The radius of the bottom of the cylinder.


**fill** - [[Boolean]]

Whether or not the cylinder is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the cylinder.


**outline** - [[Boolean]]

Whether or not the cylinder is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the cylinder outline.


**outlineWidth** - [[Double]]

The width of the cylinder outline.

Default: `1.0`


**numberOfVerticalLines** - [[Double]]

The number of vertical lines to draw along the perimeter for the outline.


**slices** - [[Double]]

The number of edges around the perimeter of the cylinder.


**shadows** - [[ShadowMode]]

Whether or not the cylinder casts or receives shadows.

Default: `DISABLED`


