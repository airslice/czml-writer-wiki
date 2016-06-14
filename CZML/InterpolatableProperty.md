This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#InterpolatableProperty

The base schema for a property whose value may be determined by interpolating over provided time-tagged samples.

**Interpolatable**: no

##Properties

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


