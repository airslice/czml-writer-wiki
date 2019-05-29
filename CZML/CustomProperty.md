This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# CustomProperty

A custom property.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

**Interpolatable**: yes

## Properties

**boolean** - [[BooleanValue]]

The property specified as a boolean value.


**boundingRectangle** - [[BoundingRectangleValue]]

The property specified as `[X, Y, Width, Height]`.


**cartesian** - [[Cartesian3Value]]

The property specified as a three-dimensional Cartesian value `[X, Y, Z]`.


**cartographicRadians** - [[CartographicRadiansValue]]

The property specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in radians and Height is in meters.


**cartographicDegrees** - [[CartographicDegreesValue]]

The property specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height]`, where Longitude and Latitude are in degrees and Height is in meters.


**cartesian2** - [[Cartesian2Value]]

The property specified as a two-dimensional Cartesian value `[X, Y]`.


**unitCartesian** - [[UnitCartesian3Value]]

The property specified as a three-dimensional unit magnitude Cartesian value `[X, Y, Z]`.


**spherical** - [[SphericalValue]]

The property specified as a spherical value `[Clock, Cone, Magnitude]`. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**unitSpherical** - [[UnitSphericalValue]]

The property specified as a unit spherical value `[Clock, Cone]`. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis.


**rgba** - [[RgbaValue]]

The property specified as an array of color components `[Red, Green, Blue, Alpha]` where each component is an integer in the range 0-255.


**rgbaf** - [[RgbafValue]]

The property specified as an array of color components `[Red, Green, Blue, Alpha]` where each component is a double in the range 0.0-1.0.


**colorBlendMode** - [[ColorBlendModeValue]]

The property specified as a color blend mode.


**cornerType** - [[CornerTypeValue]]

The property specified as a corner style.


**heightReference** - [[HeightReferenceValue]]

The property specified as a height reference.


**horizontalOrigin** - [[HorizontalOriginValue]]

The property specified as a horizontal origin.


**labelStyle** - [[LabelStyleValue]]

The property specified as a label style.


**number** - [[DoubleValue]]

The property specified as a number.


**nearFarScalar** - [[NearFarScalarValue]]

The property specified as four values `[NearDistance, NearValue, FarDistance, FarValue]`.


**unitQuaternion** - [[UnitQuaternionValue]]

The property specified as a 4-dimensional unit magnitude quaternion, specified as `[X, Y, Z, W]`.


**shadowMode** - [[ShadowModeValue]]

The property specified as a shadow mode.


**string** - [[StringValue]]

The property specified as a string.


**stripeOrientation** - [[StripeOrientationValue]]

The property specified as an orientation of stripes in the stripe material.


**wsen** - [[CartographicRectangleRadiansValue]]

The property specified as a Cartographic rectangle `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in radians.


**wsenDegrees** - [[CartographicRectangleDegreesValue]]

The property specified as a Cartographic rectangle `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in degrees.


**uri** - [[UriValue]]

The property specified as a URI.


**verticalOrigin** - [[VerticalOriginValue]]

The property specified as a vertical origin.


