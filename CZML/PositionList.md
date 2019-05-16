This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# PositionList

A list of positions.

**Interpolatable**: no

## Properties

**referenceFrame** - string

The reference frame in which cartesian positions are specified. Possible values are "FIXED" and "INERTIAL".

Default: `FIXED`


**cartesian** - [[Cartesian3ListValue]]

The list of positions specified as three-dimensional Cartesian values, `[X, Y, Z, X, Y, Z, ...]`, in meters relative to the `referenceFrame`.


**cartographicRadians** - [[CartographicListValue]]

The list of positions specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height, Longitude, Latitude, Height, ...]`, where Longitude and Latitude are in radians and Height is in meters.


**cartographicDegrees** - [[CartographicListValue]]

The list of positions specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height, Longitude, Latitude, Height, ...]`, where Longitude and Latitude are in degrees and Height is in meters.


**references** - [[ReferenceListValue]]

The list of positions specified as references. Each reference is to a property that defines a single position, which may change with time.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


