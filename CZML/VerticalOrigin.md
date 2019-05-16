This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# VerticalOrigin

The vertical origin of an element, which can optionally vary over time. It controls whether the element is bottom-, center-, or top-aligned with the `position`.

**Interpolatable**: no

## Properties

**verticalOrigin** - [[VerticalOriginValue]]

The vertical origin.


**reference** - [[ReferenceValue]]

The vertical origin specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


