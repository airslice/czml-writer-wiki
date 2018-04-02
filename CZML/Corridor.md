This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

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


