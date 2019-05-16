This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# BoundingRectangle

A bounding rectangle specified by a corner, width and height.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**boundingRectangle** - [[BoundingRectangleValue]]

The bounding rectangle specified as `[X, Y, Width, Height]`.


**reference** - [[ReferenceValue]]

The bounding rectangle specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


