This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Position

Defines a position.  The position can optionally vary over time.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

##Properties

**referenceFrame** - string

The reference frame in which cartesian positions are specified. Possible values are "FIXED" and "INERTIAL". If this property is not specified, the default reference frame is "FIXED".


**cartesian** - [[Cartesian3Value]]

The position specified as a three-dimensional Cartesian value, `[X, Y, Z]`, in meters relative to the `referenceFrame`.


**cartographicRadians** - [[CartographicValue]]

The position specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in radians and Height is in meters.


**cartographicDegrees** - [[CartographicValue]]

The position specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in degrees and Height is in meters.


**cartesianVelocity** - [[Cartesian3VelocityValue]]

The position and velocity specified as a three-dimensional Cartesian value and its derivative, `[X, Y, Z, dX, dY, dZ]`, in meters relative to the `referenceFrame`.


**reference** - [[ReferenceValue]]

The position specified as a reference to another property.


