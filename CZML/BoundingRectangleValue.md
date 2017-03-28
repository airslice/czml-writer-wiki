This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# BoundingRectangle (value)

A near-far scalar value specified as four values `[X, Y, Width, Height]`.  If the array has four elements, the value is constant.  If it has five or more elements, they are time-tagged samples arranged as `[Time, X, Y, Width, Height, Time, X, Y, Width, Height, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

**Examples**:

```javascript
[ 45, 90, 10, 10 ]
```

```javascript
[
    0, 45, 90, 10, 10,
    300, 45, 90, 15, 10,
    600, 45, 90, 10, 14
]
```

