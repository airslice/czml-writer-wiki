This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# NearFarScalar (value)

A near-far scalar value specified as four values `[NearDistance, NearValue, FarDistance, FarValue]`.  If the array has four elements, the value is constant.  If it has five or more elements, they are time-tagged samples arranged as `[Time, NearDistance, NearValue, FarDistance, FarValue, Time, NearDistance, NearValue, FarDistance, FarValue, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 150, 2.0, 15000000, 0.5 ]
```

```javascript
[
    0, 150, 2.0, 15000000, 0.5,
    300, 150, 20, 15000000, 5.0,
    600, 150, 2.0, 15000000, 0.5
]
```

