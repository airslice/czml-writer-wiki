This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# VerticalOrigin (value)

The vertical location of an origin relative to an object's position.

**Type**: string

## Values

* `BASELINE` - If the object contains text, the origin is at the baseline of the text, otherwise the origin is at the bottom of the object.

* `BOTTOM` - The origin is at the bottom of the object.

* `CENTER` - The origin is at the vertical center between `BASELINE` and `TOP`.

* `TOP` - The origin is at the top of the object.

