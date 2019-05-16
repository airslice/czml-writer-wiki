This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# BackgroundPadding

The amount of horizontal and vertical padding, in pixels, between a label's text and its background.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

## Properties

**cartesian2** - [[Cartesian2Value]]

The background padding specified as a two-dimensional Cartesian value `[X, Y]`, in pixels, where X is the horizontal padding, and Y is the vertical padding.


**reference** - [[ReferenceValue]]

The background padding specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


