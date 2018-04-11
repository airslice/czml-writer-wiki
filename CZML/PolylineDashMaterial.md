This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# PolylineDashMaterial

A material that fills the surface of a line with a pattern of dashes.

**Interpolatable**: no

## Properties

**color** - [[Color]]

The color of the dashes on the line.

Default: `white`


**gapColor** - [[Color]]

The color of the gaps between dashes on the line.

Default: `transparent`


**dashLength** - [[Double]]

The length in screen-space pixels of a single dash and gap pattern.

Default: `16.0`


**dashPattern** - [[Integer]]

A 16-bit bitfield representing which portions along a single dashLength are the dash (1) and which are the gap (0). The default value, 255 (0000000011111111), indicates 50% gap followed by 50% dash.

Default: `255`


