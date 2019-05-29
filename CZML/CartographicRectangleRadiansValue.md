This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# CartographicRectangleRadians (value)

A two dimensional region specified as `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in radians. If the array has four elements, the value is constant. If it has five or more elements, they are time-tagged samples arranged as `[Time, WestLongitude, SouthLatitude, EastLongitude, NorthLatitude, Time, WestLongitude, SouthLatitude, EastLongitude, NorthLatitude, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

