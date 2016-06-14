This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Position

Defines a position.  The position can optionally vary over time.

**Interpolatable**: yes

##Properties

**referenceFrame** - string

The reference frame in which cartesian positions are specified. Possible values are "FIXED" and "INERTIAL". If this property is not specified, the default reference frame is "FIXED".


**cartesian** - [[Cartesian3]]

The position specified as a three-dimensional Cartesian value, `[X, Y, Z]`, in meters relative to the `referenceFrame`.


**cartographicRadians** - [[Cartographic]]

The position specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in radians and Height is in meters.


**cartographicDegrees** - [[Cartographic]]

The position specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in degrees and Height is in meters.


**cartesianVelocity** - [[Cartesian3Velocity]]

The position and velocity specified as a three-dimensional Cartesian value and its derivative, `[X, Y, Z, dX, dY, dZ]`, in meters relative to the `referenceFrame`.


**reference** - [[Reference]]

The position specified as a reference to another property.


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


