This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Polyline

A polyline, which is a line in the scene composed of multiple segments.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the polyline is shown.

Default: `true`


**positions** - [[PositionList]] - **Required**

The array of positions defining the polyline as a line strip.


**arcType** - [[ArcType]]

The type of arc that should connect the positions of the polyline.

Default: `GEODESIC`


**width** - [[Double]]

The width of the polyline.

Default: `1.0`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**material** - [[PolylineMaterial]]

The material to use to draw the polyline.

Default: `solid white`


**followSurface** - [[Boolean]]

Whether or not the positions are connected as great arcs (the default) or as straight lines. This property has been superseded by arcType, which should be used instead.

Default: `true`


**shadows** - [[ShadowMode]]

Whether or not the polyline casts or receives shadows.

Default: `DISABLED`


**depthFailMaterial** - [[PolylineMaterial]]

The material to use to draw the polyline when it is below the terrain.


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying at what distance from the camera this polyline will be displayed.


**clampToGround** - [[Boolean]]

Whether or not the polyline should be clamped to the ground.

Default: `false`


**zIndex** - [[Integer]]

The z-index of the polyline, used for ordering ground geometry. Only has an effect if the polyline is constant, and `clampToGround` is true.

Default: `0`


