This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Point

A point, or viewport-aligned circle.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the point is shown.

Default: `true`


**pixelSize** - [[Double]]

The size of the point, in pixels.

Default: `1.0`


**heightReference** - [[HeightReference]]

The height reference of the point, which indicates if the position is relative to terrain or not.

Default: `NONE`


**color** - [[Color]]

The color of the point.


**outlineColor** - [[Color]]

The color of the outline of the point.


**outlineWidth** - [[Double]]

The width of the outline of the point.

Default: `0.0`


**scaleByDistance** - [[NearFarScalar]]

How the point's scale should change based on the point's distance from the camera.  This scalar value will be multiplied by `pixelSize`.


**translucencyByDistance** - [[NearFarScalar]]

How the point's translucency should change based on the point's distance from the camera.  This scalar value should range from 0 to 1.


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this point will be displayed.


**disableDepthTestDistance** - [[Double]]

The distance from the camera at which to disable the depth test. This can be used to prevent clipping against terrain, for example. When set to zero, the depth test is always applied. When set to Infinity, the depth test is never applied.


