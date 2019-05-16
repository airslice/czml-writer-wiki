This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# EllipsoidRadii

The radii of an ellipsoid.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**cartesian** - [[Cartesian3Value]]

The radii specified as a three-dimensional Cartesian value `[X, Y, Z]`, in world coordinates in meters.


**reference** - [[ReferenceValue]]

The radii specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


