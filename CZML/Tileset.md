This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Tileset

A 3D Tiles tileset.

**Interpolatable**: no

## Properties

**show** - [[Boolean]]

Whether or not the tileset is shown.

Default: `true`


**uri** - [[Uri]] - **Required**

The URI of a 3D tiles tileset. For broadest client compatibility, the URI should be accessible via Cross-Origin Resource Sharing (CORS).


**maximumScreenSpaceError** - [[Double]]

The maximum screen space error used to drive level of detail refinement.


