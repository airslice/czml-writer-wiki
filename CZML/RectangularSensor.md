This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# RectangularSensor

A rectangular pyramid sensor volume taking into account occlusion of an ellipsoid, i.e., the globe.

_Note: This type is an extension and may not be implemented by all CZML clients._

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the entire rectangular pyramid sensor is shown.

Default: `true`


**xHalfAngle** - [[Double]]

The X half angle.

Default: `PI / 2`


**yHalfAngle** - [[Double]]

The Y half angle.

Default: `PI / 2`


**radius** - [[Double]]

The radial limit of the sensor.

Default: `Infinity`


**showIntersection** - [[Boolean]]

Whether or not the intersection of the sensor with the Earth is shown.

Default: `true`


**intersectionColor** - [[Color]]

The color of the intersection of the sensor with the Earth.

Default: `white`


**intersectionWidth** - [[Double]]

The width of the intersection in pixels.

Default: `1.0`


**showLateralSurfaces** - [[Boolean]]

Whether or not the lateral surfaces, i.e., the outer sides of the sensor, are shown.

Default: `true`


**lateralSurfaceMaterial** - [[Material]]

The material to use for the sensor's lateral surface, i.e., the outer sides of the sensor.

Default: `solid white`


**showEllipsoidSurfaces** - [[Boolean]]

Whether or not ellipsoid surfaces are shown.

Default: `true`


**ellipsoidSurfaceMaterial** - [[Material]]

The material to use for the sensor's ellipsoid surfaces.

Default: `solid white`


**showEllipsoidHorizonSurfaces** - [[Boolean]]

Whether or not ellipsoid horizon surfaces are shown.

Default: `true`


**ellipsoidHorizonSurfaceMaterial** - [[Material]]

The material to use for the sensor's ellipsoid horizon surfaces.

Default: `solid white`


**showDomeSurfaces** - [[Boolean]]

Whether or not dome surfaces are shown.

Default: `true`


**domeSurfaceMaterial** - [[Material]]

The material to use for the sensor's dome surfaces.

Default: `solid white`


**portionToDisplay** - [[SensorVolumePortionToDisplay]]

What part of the sensor should be displayed.

Default: `COMPLETE`


**environmentConstraint** - [[Boolean]]

Whether or not the sensor will intersect the environment, e.g. terrain or models.

Default: `false`


**showEnvironmentOcclusion** - [[Boolean]]

Whether or not the portion of the terrain occluded by the environment will be drawn with a separate material.

Default: `false`


**environmentOcclusionMaterial** - [[Material]]

The material to use for the portion of the sensor occluded by the environment.

Default: `solid white`


**showEnvironmentIntersection** - [[Boolean]]

Whether or not a line showing where the sensor intersects the environment will be drawn.

Default: `false`


**environmentIntersectionColor** - [[Color]]

The color of the intersection line between the sensor and the environment.

Default: `white`


**environmentIntersectionWidth** - [[Double]]

The width in meters of the intersection line between the sensor and the environment.

Default: `5.0`


