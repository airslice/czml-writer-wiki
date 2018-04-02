This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Color

A color. The color can optionally vary over time.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**rgba** - [[RgbaValue]]
The color specified as an array of color components `[Red, Green, Blue, Alpha]` where each component is an integer in the range 0-255.


**rgbaf** - [[RgbafValue]]
The color specified as an array of color components `[Red, Green, Blue, Alpha]` where each component is a double in the range 0.0-1.0.


**reference** - [[ReferenceValue]]
The color specified as a reference to another property.


