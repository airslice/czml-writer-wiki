This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# StripeMaterial

A material that fills the surface with alternating colors.

**Interpolatable**: no

## Properties

**orientation** - [[StripeOrientation]]

The value indicating if the stripes are horizontal or vertical.

Default: `HORIZONTAL`


**evenColor** - [[Color]]

The even color.

Default: `white`


**oddColor** - [[Color]]

The odd color.

Default: `black`


**offset** - [[Double]]

The value indicating where in the pattern to begin drawing, with 0.0 being the beginning of the even color, 1.0 the beginning of the odd color, 2.0 being the even color again, and any multiple or fractional values being in between.

Default: `0.0`


**repeat** - [[Double]]

The number of times the stripes repeat.

Default: `1.0`


