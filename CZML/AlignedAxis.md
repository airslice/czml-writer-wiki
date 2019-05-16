This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# AlignedAxis

An aligned axis represented by a unit vector which can optionally vary over time.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**unitCartesian** - [[UnitCartesian3Value]]

The axis specified as a three-dimensional unit magnitude Cartesian value `[X, Y, Z]`, in world coordinates.


**unitSpherical** - [[UnitSphericalValue]]

The axis specified as a unit spherical value `[Clock, Cone]`, in radians. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**reference** - [[ReferenceValue]]

The axis specified as a reference to another property.


**velocityReference** - [[ReferenceValue]]

The axis specified as the normalized velocity vector of a position property. The reference must be to a `position` property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


