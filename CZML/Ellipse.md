This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Ellipse

An ellipse, which is a closed curve on or above the surface of the Earth.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the ellipse is shown.

**Default**: `true`


**semiMajorAxis** - [[Double]]

The length of the ellipse's semi-major axis in meters.


**semiMinorAxis** - [[Double]]

The length of the ellipse's semi-minor axis in meters.


**height** - [[Double]]

The altitude of the ellipse relative to the surface.


**extrudedHeight** - [[Double]]

The altitude of the ellipse's extruded face relative to the surface.


**rotation** - [[Double]]

The angle from north (counter-clockwise) in radians.


**stRotation** - [[Double]]

The rotation of any applied texture coordinates.


**granularity** - [[Double]]

The sampling distance, in radians.


**fill** - [[Boolean]]

Whether or not the ellipse is filled.

**Default**: `true`


**material** - [[Material]]

The material to use to fill the ellipse.


**outline** - [[Boolean]]

Whether or not the ellipse is outlined.

**Default**: `false`


**outlineColor** - [[Color]]

The color of the ellipse outline.


**outlineWidth** - [[Double]]

The width of the ellipse outline.

**Default**: `1.0`


**numberOfVerticalLines** - [[Double]]

The number of vertical lines to use when outlining an extruded ellipse.


