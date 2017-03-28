This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Path

A path, which is a polyline defined by the motion of an object over time.  The possible vertices of the path are specified by the `position` property.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the path is shown.

Default: `true`


**width** - [[Double]]

The width of the path line.

Default: `1.0`


**resolution** - [[Double]]

The maximum step-size, in seconds, used to sample the path.  If the `position` property has data points farther apart than resolution specifies, additional steps will be taken, creating a smoother path.

Default: `60.0`


**leadTime** - [[Double]]

The time ahead of the animation time, in seconds, to show the path.


**trailTime** - [[Double]]

The time behind the animation time, in seconds, to show the path.


**material** - [[PolylineMaterial]]

The material to use to draw the path.


