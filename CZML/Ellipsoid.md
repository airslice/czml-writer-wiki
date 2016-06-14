This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Ellipsoid

A closed quadric surface that is a three dimensional analogue of an ellipse.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the ellipsoid is shown.


**radii** - [[EllipsoidRadii]]

The dimensions of the ellipsoid.


**fill** - [[Boolean]]

Whether or not the ellipsoid is filled.


**material** - [[Material]]

The material to display on the surface of the ellipsoid.


**outline** - [[Boolean]]

Whether or not the ellipsoid is outlined.


**outlineColor** - [[Color]]

The color of the ellipsoid outline.


**outlineWidth** - [[Double]]

The width of the ellipsoid outline.


**stackPartitions** - [[Double]]

The number of times to partition the ellipsoid into stacks.


**slicePartitions** - [[Double]]

The number of times to partition the ellipsoid into radial slices.


**subdivisions** - [[Double]]

The number of points per outline line, determining the granularity of the curvature.


