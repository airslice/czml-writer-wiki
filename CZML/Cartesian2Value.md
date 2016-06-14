This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Cartesian2 (value)

A two-dimensional Cartesian value specified as `[X, Y]`.  If the array has two elements, the value is constant.  If it has three or more elements, they are time-tagged samples arranged as `[Time, X, Y, Time, X, Y, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

