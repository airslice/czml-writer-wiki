This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Direction

A unit vector, in world coordinates, that defines a direction.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**spherical** - [[SphericalValue]]

The direction specified as a spherical value `[Clock, Cone, Magnitude]`, with angles in radians and magnitude in meters. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**unitSpherical** - [[UnitSphericalValue]]

The direction specified as a unit spherical value `[Clock, Cone]`, in radians. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**cartesian** - [[Cartesian3Value]]

The direction specified as a three-dimensional Cartesian value `[X, Y, Z]`, in world coordinates in meters.


**unitCartesian** - [[UnitCartesian3Value]]

The direction specified as a three-dimensional unit magnitude Cartesian value `[X, Y, Z]`, in world coordinates in meters.


**reference** - [[ReferenceValue]]

The direction specified as a reference to another property.


