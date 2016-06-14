This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#EyeOffset

An offset in eye coordinates which can optionally vary over time.  Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis poitns up, and the Z-axis points into the screen.

**Interpolatable**: yes

##Properties

**cartesian** - [[Cartesian3]]

The eye offset specified as a three-dimensional Cartesian value `[X, Y, Z]`, in eye coordinates in meters.  If the array has three elements, the eye offset is constant.  If it has four or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, Time, X, Y, Z, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.


**reference** - [[Reference]]

The eye offset specified as a reference to another property.


**epoch** - string

The epoch to use for times specified as seconds since an epoch.


**interpolationAlgorithm** - string

The interpolation algorithm to use when interpolating. Valid values are "LINEAR", "LAGRANGE", and "HERMITE".


**interpolationDegree** - number

The degree of interpolation to use when interpolating.


**forwardExtrapolationType** - string

The type of extrapolation to perform when a value is requested at a time after any available samples. Valid values are "NONE", "HOLD", and "EXTRAPOLATE".


**forwardExtrapolationDuration** - number

The amount of time to extrapolate forward before the property becomes undefined.  A value of 0 will extrapolate forever.


**backwardExtrapolationType** - string

The type of extrapolation to perform when a value is requested at a time before any available samples. Valid values are "NONE", "HOLD", and "EXTRAPOLATE".


**backwardExtrapolationDuration** - number

The amount of time to extrapolate backward before the property becomes undefined.  A value of 0 will extrapolate forever.


