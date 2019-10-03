This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Ellipsoid

A closed quadric surface that is a three-dimensional analogue of an ellipse.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the ellipsoid is shown.

Default: `true`


**radii** - [[EllipsoidRadii]] - **Required**

The radii of the ellipsoid.


**innerRadii** - [[EllipsoidRadii]]

The inner radii of the ellipsoid.


**minimumClock** - [[Double]]

The minimum clock angle of the ellipsoid.

Default: `0.0`


**maximumClock** - [[Double]]

The maximum clock angle of the ellipsoid.

Default: `2π`


**minimumCone** - [[Double]]

The minimum cone angle of the ellipsoid.

Default: `0.0`


**maximumCone** - [[Double]]

The maximum cone angle of the ellipsoid.

Default: `π`


**heightReference** - [[HeightReference]]

The height reference of the ellipsoid, which indicates if the position is relative to terrain or not.

Default: `NONE`


**fill** - [[Boolean]]

Whether or not the ellipsoid is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the ellipsoid.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the ellipsoid is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the ellipsoid outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the ellipsoid outline.

Default: `1.0`


**stackPartitions** - [[Integer]]

The number of times to partition the ellipsoid into stacks.

Default: `64`


**slicePartitions** - [[Integer]]

The number of times to partition the ellipsoid into radial slices.

Default: `64`


**subdivisions** - [[Integer]]

The number of samples per outline ring, determining the granularity of the curvature.

Default: `128`


**shadows** - [[ShadowMode]]

Whether or not the ellipsoid casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying at what distance from the camera this ellipsoid will be displayed.


