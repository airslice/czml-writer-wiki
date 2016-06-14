This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Polyline

A polyline, which is a line in the scene composed of multiple segments.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the polyline is shown.


**positions** - [[PositionList]]

The array of positions defining the polyline as a line strip.


**material** - [[PolylineMaterial]]

The material to use to draw the polyline.


**width** - [[Double]]

The width of the polyline.


**followSurface** - [[Boolean]]

Whether or not the positions are connected as great arcs (the default) or as straight lines.

