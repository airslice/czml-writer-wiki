This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# GridMaterial

A material that fills the surface with a two dimensional grid.

**Interpolatable**: no

## Properties

**color** - [[Color]]

The color of the surface.

Default: `white`


**cellAlpha** - [[Double]]

The alpha value for the space between grid lines. This will be combined with the color alpha.

Default: `0.1`


**lineCount** - [[LineCount]]

The number of grid lines along each axis.

Default: `[8, 8]`


**lineThickness** - [[LineThickness]]

The thickness of grid lines along each axis, in pixels.

Default: `[1.0, 1.0]`


**lineOffset** - [[LineOffset]]

The offset of grid lines along each axis, as a percentage from 0 to 1.

Default: `[0.0, 0.0]`


