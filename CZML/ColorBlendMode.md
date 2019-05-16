This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# ColorBlendMode

Defines different modes for blending between a target color and an entity's source color.

**Interpolatable**: no

## Properties

**colorBlendMode** - [[ColorBlendModeValue]]

The color blend mode.


**reference** - [[ReferenceValue]]

The color blend mode specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


