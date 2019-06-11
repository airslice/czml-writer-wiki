This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# CartographicRectangleDegrees (value)

A two-dimensional region specified as `[WestLongitude, SouthLatitude, EastLongitude, NorthLatitude]`, with values in degrees. If the array has four elements, the value is constant. If it has five or more elements, they are time-tagged samples arranged as `[Time, WestLongitude, SouthLatitude, EastLongitude, NorthLatitude, Time, WestLongitude, SouthLatitude, EastLongitude, NorthLatitude, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ -120.0, 40.0, -110.0, 50.0 ]
```

```javascript
[
    0, -120.0, 40.0, -110.0, 50.0,
    300, -125.0, 40.0, -110.0, 50.0,
    600, -125.0, 30.0, -110.0, 45.0
]
```

