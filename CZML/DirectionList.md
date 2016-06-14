This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#DirectionList

A list of directions.

**Interpolatable**: no

##Properties

**spherical** - [[SphericalList]]

The list of directions specified as spherical values `[Clock, Cone, Magnitude, Clock, Cone, Magnitude, ...]`, with angles in radians and magnitude in meters.  The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis.  The cone angle is the angle from the positive Z axis toward the negative Z axis.


**unitSpherical** - [[UnitSphericalList]]

The list of directions specified as unit spherical values `[Clock, Cone, Clock, Cone, ...]`, in radians.  The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis.  The cone angle is the angle from the positive Z axis toward the negative Z axis.


**cartesian** - [[Cartesian3List]]

The list of directions specified as three-dimensional Cartesian values `[X, Y, Z, X, Y, Z, ...]`, in world coordinates in meters.


**unitCartesian** - [[UnitCartesian3List]]

The list of directions specified as three-dimensional unit magnitude Cartesian values, `[X, Y, Z, X, Y, Z, ...]`, in world coordinates in meters.


