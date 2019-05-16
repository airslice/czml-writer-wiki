This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Rotation

Defines a rotation that transforms a vector expressed in one axes and transforms it to another.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

**Examples**:

```javascript
{
    "rotation": {
        "unitQuaternion": [ 0.0, 0.0, 0.0, 1.0 ]
    }
}
```

```javascript
{
    "rotation": {
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

The rotation specified as a 4-dimensional unit magnitude quaternion, specified as `[X, Y, Z, W]`.


**reference** - [[ReferenceValue]]

The rotation specified as a reference to another property.


**delete** - boolean

Whether the client should delete existing samples or interval data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


