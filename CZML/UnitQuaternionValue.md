This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# UnitQuaternion (value)

A set of 4-dimensional coordinates used to represent rotation in 3-dimensional space, specified as `[X, Y, Z, W]`.  If the array has four elements, the value is constant.  If it has five or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, W, Time, X, Y, Z, W, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 0, 0, 0, 1 ]
```

```javascript
[
    0, 0.45652188368372576, -0.049580035995243577, -0.8819344359461565, 0.10640131785324795,
    300, 0.309688526062018, -0.0592870464529779, -0.945283886004075, 0.0837641797515638,
    600, 0.15524757622990795, -0.06613430791377527, -0.9841132393764626, 0.05518673278488507
]
```

