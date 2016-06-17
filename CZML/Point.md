This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Point

A point, or viewport-aligned circle.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the point is shown.

Default: `true`


**pixelSize** - [[Double]]

The size of the point, in pixels.

Default: `1.0`


**color** - [[Color]]

The color of the point.


**outlineColor** - [[Color]]

The color of the outline of the point.


**outlineWidth** - [[Double]]

The width of the outline of the point.

Default: `0.0`


**scaleByDistance** - [[NearFarScalar]]

How the point's scale should change based on the point's distance from the camera.  This scalar value will be multiplied by `scale`.


**translucencyByDistance** - [[NearFarScalar]]

How the point's translucency should change based on the point's distance from the camera.  This scalar value should range from 0 to 1.


