This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# HeightReference (value)

The height reference of an object, which indicates if the object's position is relative to terrain or not.

**Type**: string

## Values

* `NONE` - The position is absolute.

* `CLAMP_TO_GROUND` - The position is clamped to the terrain.

* `RELATIVE_TO_GROUND` - The position height is the height above the terrain.

