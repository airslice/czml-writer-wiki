This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# NearFarScalar

A numeric value which will be linearly interpolated between two values based on an object's distance from the camera, in eye coordinates. The computed value will interpolate between the near value and the far value while the camera distance falls between the near distance and the far distance, and will be clamped to the near or far value while the distance is less than the near distance or greater than the far distance, respectively.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

**Interpolatable**: yes

## Properties

**nearFarScalar** - [[NearFarScalarValue]]

The value specified as four values `[NearDistance, NearValue, FarDistance, FarValue]`, with distances in eye coordinates in meters.


**reference** - [[ReferenceValue]]

The value specified as a reference to another property.


