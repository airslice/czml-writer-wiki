This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Polygon

A polygon, which is a closed figure on the surface of the Earth.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the polygon is shown.

Default: `true`


**positions** - [[PositionList]]

The array of positions defining a simple polygon.


**height** - [[Double]]

The height of the polygon when `perPositionHeight` is false.


**extrudedHeight** - [[Double]]

The extruded height of the polygon.


**stRotation** - [[Double]]

The rotation of any applied texture. A positive rotation is counter-clockwise.


**granularity** - [[Double]]

The sampling distance, in radians.


**fill** - [[Boolean]]

Whether or not the polygon is filled.

Default: `true`


**material** - [[Material]]

The material to use to fill the polygon.


**outline** - [[Boolean]]

Whether or not the polygon is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the polygon outline.


**outlineWidth** - [[Double]]

The width of the polygon outline.

Default: `1.0`


**perPositionHeight** - [[Boolean]]

Whether to use the height of each position to define the polygon or to use `height` as a constant height above the surface.


**closeTop** - [[Boolean]]

Whether to close the top of the polygon.

Default: `true`


**closeBottom** - [[Boolean]]

Whether to close the bottom of the polygon.

Default: `true`


**shadows** - [[ShadowMode]]

Whether or not the polygon casts or receives shadows.

Default: `DISABLED`


