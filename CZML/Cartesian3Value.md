This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Cartesian3 (value)

A three-dimensional Cartesian value specified as `[X, Y, Z]`.  If the array has three elements, the value is constant.  If it has four or more elements, they are time-tagged samples arranged as `[Time, X, Y, Z, Time, X, Y, Z, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 1.0, 2.0, 3.0 ]
```

```javascript
[
    0, 4650397.56551457, -3390535.52275848, -4087729.48877329,
    300, 3169722.12564676, -2787480.80604407, -5661647.74541255,
    600, 1369743.14695017, -1903662.23809705, -6663952.07552171
]
```

