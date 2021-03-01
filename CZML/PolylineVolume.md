This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# PolylineVolume

A polyline with a volume, defined as a 2D shape extruded along a polyline that conforms to the curvature of the globe.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the volume is shown.

Default: `true`


**positions** - [[PositionList]] - **Required**

The array of positions defining the center of the polyline volume.


**shape** - [[Shape]] - **Required**

The array of positions defining the shape of the volume to be extruded.


**cornerType** - [[CornerType]]

The style of the corners of the volume.

Default: `ROUNDED`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `π / 180.0`


**fill** - [[Boolean]]

Whether or not the volume is filled.

Default: `true`


**material** - [[Material]]

The material to use to fill the volume.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the volume is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the volume outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the volume outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the volume casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this volume will be displayed.


