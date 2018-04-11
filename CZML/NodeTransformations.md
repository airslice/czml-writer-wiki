This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# NodeTransformations

A mapping of node names to node transformations.

**Interpolatable**: no

**Examples**:

```javascript
{
    "nodeTransformations": {
        "node1": {
            "scale": {
                "cartesian": [
                    1.0, 2.0, 3.0
                ]
            },
            "rotation": {
                "unitQuaternion": [
                    0.0, 0.0, 0.0, 1.0
                ]
            },
            "translation": {
                "cartesian": [
                    4.0, 5.0, 6.0
                ]
            }
        },
        "node2": {
            "scale": {
                "epoch": "2012-04-02T12:00:00Z",
                "cartesian": [
                    0.0, 1.0, 2.0, 3.0,
                    60.0, 10.0, 12.0, 14.0
                ]
            }
        }
    }
}
```

This type represents a key-value mapping, where values are of type [[NodeTransformation]].

