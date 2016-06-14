This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#RectangularSensor

A rectangular pyramid sensor volume taking into account occlusion of an ellipsoid, i.e., the globe.

_Note: This type is an extension and may not be implemented by all CZML clients._

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the entire rectangular pyramid sensor is shown.


**xHalfAngle** - [[Double]]

The X half angle.


**yHalfAngle** - [[Double]]

The Y half angle.


**radius** - [[Double]]

The radial limit of the pyramid.


**showIntersection** - [[Boolean]]

Whether or not the intersection of the pyramid with the Earth is shown.


**intersectionColor** - [[Color]]

The color of the intersection of the pyramid with the Earth.


**intersectionWidth** - [[Double]]

The width of the intersection in pixels.


**showLateralSurfaces** - [[Boolean]]

Whether or not the lateral surfaces of the pyramid are shown.


**lateralSurfaceMaterial** - [[Material]]

The material to use for the pyramid's lateral surfaces.


**showEllipsoidSurfaces** - [[Boolean]]

Whether or not ellipsoid surfaces are shown.


**ellipsoidSurfaceMaterial** - [[Material]]

The material to use for the pyramid's ellipsoid surfaces.


**showEllipsoidHorizonSurfaces** - [[Boolean]]

Whether or not ellipsoid horizon surfaces are shown.


**ellipsoidHorizonSurfaceMaterial** - [[Material]]

The material to use for the pyramid's ellipsoid horizon surfaces.


**showDomeSurfaces** - [[Boolean]]

Whether or not dome surfaces are shown.


**domeSurfaceMaterial** - [[Material]]

The material to use for the pyramid's dome surfaces.


**portionToDisplay** - [[SensorVolumePortionToDisplay]]

What part of the sensor should be displayed.


**environmentConstraint** - [[Boolean]]

Whether or not the sensor will intersect the environment, e.g. terrain or models.


**showEnvironmentOcclusion** - [[Boolean]]

Whether or not the portion of the terrain occluded by the environment will be drawn with a separate material.


**environmentOcclusionMaterial** - [[Material]]

The material to use for the portion of the sensor occluded by the environment.


**showEnvironmentIntersection** - [[Boolean]]

Whether or not a line showing where the sensor intersects the environment will be drawn.


**environmentIntersectionColor** - [[Color]]

The color of the intersection line between the sensor and the environment.


**environmentIntersectionWidth** - [[Double]]

The width in meters of the intersection line between the sensor and the environment.

