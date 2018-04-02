This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# EyeOffset

An offset in eye coordinates which can optionally vary over time.  Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis poitns up, and the Z-axis points into the screen.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**cartesian** - [[Cartesian3Value]]
The eye offset specified as a three-dimensional Cartesian value `[X, Y, Z]`, in eye coordinates in meters.  If the array has three elements, the eye offset is constant.  If it has four or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, Time, X, Y, Z, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.


**reference** - [[ReferenceValue]]
The eye offset specified as a reference to another property.


