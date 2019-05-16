This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# LabelStyle

The style of a label.

**Interpolatable**: no

## Properties

**labelStyle** - [[LabelStyleValue]]

The label style.


**reference** - [[ReferenceValue]]

The label style specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


