This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# ViewFrom

A suggested initial camera position offset when tracking this object, specified as a Cartesian position. Typically defined in the East (x), North (y), Up (z) reference frame relative to the object's position, but may use another frame depending on the object's velocity.

**Extends**: [[InterpolatableProperty]]

**Extends**: [[DeletableProperty]]

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

The offset specified as a three-dimensional Cartesian value `[X, Y, Z]`.


**reference** - [[ReferenceValue]]

The offset specified as a reference to another property.


