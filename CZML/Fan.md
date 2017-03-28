This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Fan

A fan.  A fan starts at a point or apex and extends in a specified list of directions from the apex.  Each pair of directions forms a face of the fan extending to the specified radius.

_Note: This type is an extension and may not be implemented by all CZML clients._

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the fan is shown.


**directions** - [[DirectionList]]

The list of directions defining the fan.


**radius** - [[Double]]

The radial limit of the fan.


**perDirectionRadius** - [[Boolean]]

Whether the magnitude of each direction is used instead of a constant radius.


**material** - [[Material]]

The material to display on the surface of the fan.


**fill** - [[Boolean]]

Whether or not the fan is filled.


**outline** - [[Boolean]]

Whether or not the fan is outlined.


**outlineColor** - [[Color]]

The color of the fan outline.


**outlineWidth** - [[Double]]

The width of the fan outline.


**numberOfRings** - [[Double]]

The number of outline rings to draw, starting from the outer edge and equidistantly spaced towards the center.


