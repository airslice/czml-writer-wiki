This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Cartesian3Velocity

A three-dimensional Cartesian value and its derivative specified as `[X, Y, Z, dX, dY, dZ]`.  If the array has six elements, the value is constant.  If it has seven or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, dX, dY, dZ, Time, X, Y, Z, dX, dY, dZ, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

