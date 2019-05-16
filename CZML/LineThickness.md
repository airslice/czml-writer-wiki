This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# LineThickness

The thickness of grid lines along each axis, in pixels.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**cartesian2** - [[Cartesian2Value]]

The thickness specified as a two-dimensional Cartesian value `[X, Y]`, in pixels.


**reference** - [[ReferenceValue]]

The thickness specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


