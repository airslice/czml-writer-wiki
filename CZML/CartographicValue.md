This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Cartographic (value)

A geodetic, WGS84 position specified as `[Longitude, Latitude, Height]`. If the array has three elements, the value is constant. If it has four or more elements, they are time-tagged samples arranged as `[Time, Longitude, Latitude, Height, Time, Longitude, Latitude, Height, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 1.0, 2.0, 3.0 ]
```

```javascript
[
    0, -77, 37, 100000,
    300, -77.5, 37, 100500,
    600, -77.9, 37, 100900
]
```

