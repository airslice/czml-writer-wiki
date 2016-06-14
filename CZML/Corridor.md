This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Corridor

A corridor, which is a shape defined by a centerline and width that conforms to the curvature of the globe. It can be placed on the surface or at altitude and can optionally be extruded into a volume.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the corridor is shown.


**width** - [[Double]]

The width of the corridor, which is the distance between the edges of the corridor.


**height** - [[Double]]

The height of the corridor, which is the altitude of the corridor relative to the surface.


**extrudedHeight** - [[Double]]

The extruded height of the corridor, which is the altitude of the corridor's extruded face relative to the surface.


**cornerType** - [[CornerType]]

The style of the corners of the corridor.


**granularity** - [[Double]]

The sampling distance, in radians.


**fill** - [[Boolean]]

Whether or not the corridor is filled.


**material** - [[Material]]

The material to display on the surface of the corridor.


**outline** - [[Boolean]]

Whether or not the corridor is outlined.


**outlineColor** - [[Color]]

The color of the corridor outline.


**outlineWidth** - [[Double]]

The width of the corridor outline.


