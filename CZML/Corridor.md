This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Corridor

A corridor, which is a shape defined by a centerline and width that conforms to the curvature of the globe. It can be placed on the surface or at altitude and can optionally be extruded into a volume.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the corridor is shown.

Default: `true`


**positions** - [[PositionList]] - **Required**

The array of positions defining the centerline of the corridor.


**width** - [[Double]] - **Required**

The width of the corridor, which is the distance between the edges of the corridor.


**height** - [[Double]]

The height of the corridor, which is the altitude of the corridor relative to the surface.

Default: `0.0`


**extrudedHeight** - [[Double]]

The extruded height of the corridor, which is the altitude of the corridor's extruded face relative to the surface.


**heightReference** - [[HeightReference]]

The height reference of the corridor, which indicates if `height` is relative to terrain or not.

Default: `NONE`


**extrudedHeightReference** - [[HeightReference]]

The extruded height reference of the corridor, which indicates if `extrudedHeight` is relative to terrain or not.

Default: `NONE`


**cornerType** - [[CornerType]]

The style of the corners of the corridor.

Default: `ROUNDED`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**fill** - [[Boolean]]

Whether or not the corridor is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the corridor.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the corridor is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the corridor outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the corridor outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the corridor casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this corridor will be displayed.


**zIndex** - [[Integer]]

The z-index of the corridor, used for ordering ground geometry. Only has an effect if the corridor is constant, and `height` and `extrudedHeight` are not specified.

Default: `0`


