This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# ViewFrom

A suggested camera location when viewing an object, specified as a Cartesian position in the East (x), North (y), Up (z) reference frame relative to the object's position.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

**Examples**:

```javascript
{
    "viewFrom": {
        "cartesian": [ 4.3, 0.1, 2.6 ]
    }
}
```

## Properties

**cartesian** - [[Cartesian3Value]]
The camera location specified as a three-dimensional Cartesian value `[X, Y, Z]`, in the East (x), North (y), Up (z) reference frame relative to the object's position.


**reference** - [[ReferenceValue]]
The camera location specified as a reference to another property.


