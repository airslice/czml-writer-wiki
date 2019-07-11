This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# PositionListOfLists

A list of lists of positions.

**Extends**: [[DeletableProperty]]

**Interpolatable**: no

## Properties

**cartesian** - [[Cartesian3ListOfListsValue]]

The list of lists of positions specified as three-dimensional Cartesian values, `[X, Y, Z, X, Y, Z, ...]`, in meters relative to the `referenceFrame`.


**cartographicRadians** - [[CartographicRadiansListOfListsValue]]

The list of lists of positions specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height, Longitude, Latitude, Height, ...]`, where Longitude and Latitude are in radians and Height is in meters.


**cartographicDegrees** - [[CartographicDegreesListOfListsValue]]

The list of lists of positions specified in Cartographic WGS84 coordinates, `[Longitude, Latitude, Height, Longitude, Latitude, Height, ...]`, where Longitude and Latitude are in degrees and Height is in meters.


**references** - [[ReferenceListOfListsValue]]

The list of lists of positions specified as references. Each reference is to a property that defines a single position, which may change with time.


