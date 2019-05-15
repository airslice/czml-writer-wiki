This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Polygon

A polygon, which is a closed figure on the surface of the Earth.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the polygon is shown.

Default: `true`


**positions** - [[PositionList]] - **Required**

The array of positions defining a simple polygon.


**arcType** - [[ArcType]]

The type of arc that should connect the positions of the polygon.

Default: `GEODESIC`


**height** - [[Double]]

The height of the polygon when `perPositionHeight` is false.

Default: `0.0`


**extrudedHeight** - [[Double]]

The extruded height of the polygon.


**heightReference** - [[HeightReference]]

The height reference of the polygon, which indicates if `height` is relative to terrain or not.

Default: `NONE`


**extrudedHeightReference** - [[HeightReference]]

The extruded height reference of the polygon, which indicates if `extrudedHeight` is relative to terrain or not.

Default: `NONE`


**stRotation** - [[Double]]

The rotation of any applied texture. A positive rotation is counter-clockwise.

Default: `0.0`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**fill** - [[Boolean]]

Whether or not the polygon is filled.

Default: `true`


**material** - [[Material]]

The material to use to fill the polygon.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the polygon is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the polygon outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the polygon outline.

Default: `1.0`


**perPositionHeight** - [[Boolean]]

Whether to use the height of each position to define the polygon or to use `height` as a constant height above the surface.

Default: `false`


**closeTop** - [[Boolean]]

Whether to close the top of the polygon.

Default: `true`


**closeBottom** - [[Boolean]]

Whether to close the bottom of the polygon.

Default: `true`


**shadows** - [[ShadowMode]]

Whether or not the polygon casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this polygon will be displayed.


**zIndex** - [[Integer]]

The z-index of the polygon, used for ordering ground geometry. Only has an effect if the polygon is constant, and `height` and `extrudedHeight` are not specified.

Default: `0`


