This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#UnitCartesian3

A three-dimensional unit magnitude Cartesian value specified as `[X, Y, Z]`.  If the array has three elements, the value is constant.  If it has four or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, Time, X, Y, Z, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

