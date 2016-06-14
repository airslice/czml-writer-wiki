This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Model

A 3D model.

**Interpolatable**: no

##Properties

**show** - [[Boolean]]

Whether or not the model is shown.


**scale** - [[Double]]

The scale of the model.


**minimumPixelSize** - [[Double]]

The approximate minimum pixel size of the model regardless of zoom.


**gltf** - [[Uri]]

The URI of a <a href="https://github.com/KhronosGroup/glTF">glTF</a> model.  For broadest client compatibility, the URI should be accessible via Cross-Origin Resource Sharing (CORS).  The URI may also be a <a href="https://developer.mozilla.org/en/data_URIs">data URI</a>.


**runAnimations** - [[Boolean]]

Whether or not to run all animations defined in the glTF model.


**nodeTransformations** - [[NodeTransformations]]

A mapping of node names to node transformations.

**Examples**:

```javascript
{
    "id": "MyID",
    "model": {
        "gltf": "example.gltf",
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
}
```


