This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# CartographicRadians (value)

A geodetic, WGS84 position specified as `[Longitude, Latitude, Height]`, where Longitude and Latitude are in radians and Height is in meters. If the array has three elements, the value is constant. If it has four or more elements, they are time-tagged samples arranged as `[Time, Longitude, Latitude, Height, Time, Longitude, Latitude, Height, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

