This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Ellipse

An ellipse, which is a closed curve on or above the surface of the Earth.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the ellipse is shown.


**semiMajorAxis** - [[Double]]

The length of the ellipse's semi-major axis in meters.


**semiMinorAxis** - [[Double]]

The length of the ellipse's semi-minor axis in meters.


**rotation** - [[Double]]

The angle from north (counter-clockwise) in radians.


**material** - [[Material]]

The material to use to fill the ellipse.


**height** - [[Double]]

The height of the ellipse when perPositionHeight is false.


**extrudedHeight** - [[Double]]

The extruded height of the ellipse.


**granularity** - [[Double]]

The sampling distance, in radians.


**stRotation** - [[Double]]

The rotation of any applied texture coordinates.


**fill** - [[Boolean]]

Whether or not the ellipse is filled.


**outline** - [[Boolean]]

Whether or not the ellipse is outlined.


**outlineColor** - [[Color]]

The color of the ellipse outline.


**outlineWidth** - [[Double]]

The width of the ellipse outline.


**numberOfVerticalLines** - [[Double]]

The number of vertical lines to use when outlining an extruded ellipse.


