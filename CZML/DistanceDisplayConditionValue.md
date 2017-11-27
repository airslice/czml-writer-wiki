This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# DistanceDisplayCondition (value)

Indicates the visibility of an object based on the distance to the camera, specified as two values `[NearDistance, FarDistance]`.  If the array has two elements, the value is constant.  If it has three or more elements, they are time-tagged samples arranged as `[Time, NearDistance, FarDistance, Time, NearDistance, FarDistance, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 150, 15000000 ]
```

```javascript
[
    0, 150, 15000000,
    300, 10000, 15000000,
    600, 150, 15000000
]
```

