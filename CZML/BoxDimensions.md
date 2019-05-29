This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# BoxDimensions

The width, depth, and height of a box.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

**Interpolatable**: yes

## Properties

**cartesian** - [[Cartesian3Value]]

The dimensions specified as a three-dimensional Cartesian value `[X, Y, Z]`, with X representing width, Y representing depth, and Z representing height, in world coordinates in meters.


**reference** - [[ReferenceValue]]

The dimensions specified as a reference to another property.


