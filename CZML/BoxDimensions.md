This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#BoxDimensions

The width, depth, and height of a box.

**Interpolatable**: yes

##Properties

**cartesian** - [[Cartesian3]]

The dimensions specified as a three-dimensional Cartesian value `[X, Y, Z]`, with X representing width, Y representing depth, and Z representing height, in world coordinates in meters.


**reference** - [[Reference]]

The dimensions specified as a reference to another property.


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


