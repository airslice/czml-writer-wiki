This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# AlignedAxis

An aligned axis represented by a unit vector which can optionally vary over time.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

**Interpolatable**: yes

## Properties

**unitCartesian** - [[UnitCartesian3Value]]

The axis specified as a three-dimensional unit magnitude Cartesian value `[X, Y, Z]`, in world coordinates.


**unitSpherical** - [[UnitSphericalValue]]

The axis specified as a unit spherical value `[Clock, Cone]`, in radians. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**reference** - [[ReferenceValue]]

The axis specified as a reference to another property.


**velocityReference** - [[VelocityReferenceValue]]

The axis specified as the normalized velocity vector of a position property. The reference must be to a `position` property.


