This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Orientation

Defines an orientation.  An orientation is a rotation that takes a vector expressed in the "body" axes of the object and transforms it to the Earth fixed axes.

**Interpolatable**: yes

##Properties

**unitQuaternion** - [[UnitQuaternion]]

The orientation specified as a 4-dimensional unit magnitude quaternion, specified as `[X, Y, Z, W]`.


**reference** - [[Reference]]

The orientation specified as a reference to another property.


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


