This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# HeightReference

The height reference of an object, which indicates if the object's position is relative to terrain or not.

**Interpolatable**: no

## Properties

**heightReference** - [[HeightReferenceValue]]

The height reference.


**reference** - [[ReferenceValue]]

The height reference specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


