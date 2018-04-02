This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Vector

Defines a graphical vector that originates at the `position` property and extends in the provided direction for the provided length.

_Note: This type is an extension and may not be implemented by all CZML clients._

**Interpolatable**: no

## Properties

**show** - [[Boolean]]
Whether or not the vector is shown.


**color** - [[Color]]
The color of the vector.


**direction** - [[Direction]]
The direction of the vector.


**length** - [[Double]]
The graphical length of the vector.


**minimumLengthInPixels** - [[Double]]
The minimum graphical length of the vector in pixels.


