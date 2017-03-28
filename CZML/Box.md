This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Box

A box, which is a closed rectangular cuboid.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the box is shown.

Default: `true`


**dimensions** - [[BoxDimensions]]

The dimensions of the box.


**fill** - [[Boolean]]

Whether or not the box is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the box.


**outline** - [[Boolean]]

Whether or not the box is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the box outline.


**outlineWidth** - [[Double]]

The width of the box outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the box casts or receives shadows.

Default: `DISABLED`


