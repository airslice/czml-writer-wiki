This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# ImageMaterial

A material that fills the surface with an image.

**Interpolatable**: no

## Properties

**image** - [[Uri]]

The image to display on the surface.


**repeat** - [[Repeat]]

The number of times the image repeats along each axis.

Default: `[1, 1]`


**color** - [[Color]]

The color of the image. This color value is multiplied with the image to produce the final color.

Default: `white`


**transparent** - [[Boolean]]

Whether or not the image has transparency.

Default: `false`


