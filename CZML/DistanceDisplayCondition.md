This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# DistanceDisplayCondition

Indicates the visibility of an object based on the distance to the camera.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**distanceDisplayCondition** - [[DistanceDisplayConditionValue]]

The value specified as two values `[NearDistance, FarDistance]`, with distances in meters.


**reference** - [[ReferenceValue]]

The value specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


