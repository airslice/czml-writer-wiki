This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Wall

A two dimensional wall defined as a line strip and optional maximum and minimum heights, which conforms to the curvature of the globe and can be placed along the surface or at altitude.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the wall is shown.

Default: `true`


**positions** - [[PositionList]] - **Required**

The array of positions defining the centerline of the wall.


**minimumHeights** - [[DoubleList]]

The list of heights to be used for the bottom of the wall, instead of the surface.


**maximumHeights** - [[DoubleList]]

The list of heights to be used for the top of the wall, instead of the height of each position.


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**fill** - [[Boolean]]

Whether or not the wall is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the wall.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the wall is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the wall outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the wall outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the wall casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying at what distance from the camera this wall will be displayed.


