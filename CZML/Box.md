This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Box

A box, which is a closed rectangular cuboid.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the box is shown.

Default: `true`


**dimensions** - [[BoxDimensions]] - **Required**

The dimensions of the box.


**heightReference** - [[HeightReference]]

The height reference of the box, which indicates if the position is relative to terrain or not.

Default: `NONE`


**fill** - [[Boolean]]

Whether or not the box is filled.

Default: `true`


**material** - [[Material]]

The material to display on the surface of the box.

Default: `solid white`


**outline** - [[Boolean]]

Whether or not the box is outlined.

Default: `false`


**outlineColor** - [[Color]]

The color of the box outline.

Default: `black`


**outlineWidth** - [[Double]]

The width of the box outline.

Default: `1.0`


**shadows** - [[ShadowMode]]

Whether or not the box casts or receives shadows.

Default: `DISABLED`


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this box will be displayed.


