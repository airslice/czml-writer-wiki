This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Ellipse

An ellipse, which is a closed curve on or above the surface of the Earth.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the ellipse is shown.

Default: `true`


**semiMajorAxis** - [[Double]] - **Required**

The length of the ellipse's semi-major axis in meters.


**semiMinorAxis** - [[Double]] - **Required**

The length of the ellipse's semi-minor axis in meters.


**height** - [[Double]]

The altitude of the ellipse relative to the surface.

Default: `0.0`


**extrudedHeight** - [[Double]]

The altitude of the ellipse's extruded face relative to the surface.


**rotation** - [[Double]]

The angle from north (counter-clockwise) in radians.

Default: `0.0`


**stRotation** - [[Double]]

The rotation of any applied texture coordinates.

Default: `0.0`


**granularity** - [[Double]]

The sampling distance, in radians.

Default: `PI / 180.0`


**fill** - [[Boolean]]

Whether or not the ellipse is filled.

Default: `true`


**material** - [[Material]]

The material to use to fill the ellipse.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the ellipse is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the ellipse outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the ellipse outline.

Default: `1.0`


**numberOfVerticalLines** - [[Integer]]

The number of vertical lines to use when outlining an extruded ellipse.

Default: `16`


**shadows** - [[ShadowMode]]

Whether or not the ellipse casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying at what distance from the camera this ellipse will be displayed.


**zIndex** - [[Integer]]

The z-index of the ellipse, used for ordering ground geometry. Only has an effect if the ellipse is constant, and `height` and `extrudedHeight` are not specified.

Default: `0`


