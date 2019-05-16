This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# CornerType

The style of a corner.

**Interpolatable**: no

## Properties

**cornerType** - [[CornerTypeValue]]

The corner style.


**reference** - [[ReferenceValue]]

The corner style specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


