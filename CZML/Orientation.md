This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Orientation

Defines an orientation.  An orientation is a rotation that takes a vector expressed in the "body" axes of the object and transforms it to the Earth fixed axes.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

**Examples**:

```javascript
{
    "orientation": {
        "unitQuaternion": [ 0.0, 0.0, 0.0, 1.0 ]
    }
}
```

```javascript
{
    "orientation": {
        "interpolationAlgorithm": "LINEAR",
        "interpolationDegree": 1,
        "epoch": "2012-03-15T10:00:00Z",
        "unitQuaternion": [
            0, 0.45652188368372576, -0.049580035995243577, -0.8819344359461565, 0.10640131785324795,
            300, 0.309688526062018, -0.0592870464529779, -0.945283886004075, 0.0837641797515638,
            600, 0.15524757622990795, -0.06613430791377527, -0.9841132393764626, 0.05518673278488507
        ]
    }
}
```

## Properties

**unitQuaternion** - [[UnitQuaternionValue]]

The orientation specified as a 4-dimensional unit magnitude quaternion, specified as `[X, Y, Z, W]`.


**reference** - [[ReferenceValue]]

The orientation specified as a reference to another property.


**velocityReference** - [[ReferenceValue]]

The orientation specified as the normalized velocity vector of a position property. The reference must be to a `position` property.


