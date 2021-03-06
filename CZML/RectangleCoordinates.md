This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# RectangleCoordinates

A set of coordinates describing a cartographic rectangle on the surface of the ellipsoid.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

**Interpolatable**: yes

## Properties

**wsen** - [[CartographicRectangleRadiansValue]]

The set of coordinates specified as Cartographic values `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in radians.


**wsenDegrees** - [[CartographicRectangleDegreesValue]]

The set of coordinates specified as Cartographic values `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in degrees.


**reference** - [[ReferenceValue]]

The set of coordinates specified as a reference to another property.


