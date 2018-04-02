This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Billboard

A billboard, or viewport-aligned image. The billboard is positioned in the scene by the `position` property. A billboard is sometimes called a marker.

**Interpolatable**: no

**Examples**:

```javascript
{
    "billboard": {
        "image": [
            {
                "interval": "2013-01-01T00:00:00Z/2013-01-01T01:00:00Z",
                "uri": "image.png"
            },
            {
                "interval": "2013-01-01T01:00:00Z/2013-01-01T02:00:00Z",
                "uri": "image2.png"
            }
        ],
        "scale": 1.0,
        "pixelOffset": {
            "epoch": "2013-01-01T00:00:00Z",
            "cartesian2": [
                0.0, 1.0, 2.0,
                1.0, 3.0, 4.0
            ]
        },
        "eyeOffset": {
            "cartesian": [ 3.0, 4.0, 5.0 ]
        },
        "rotation": 1.3,
        "horizontalOrigin": "CENTER",
        "verticalOrigin": "CENTER",
        "color": {
            "rgbaf": [ 1.0, 1.0, 1.0, 1.0 ]
        },
        "alignedAxis": {
            "cartesian": [ 1.0, 0.0, 0.0 ]
        },
        "show": true,
        "sizeInMeters": false,
        "width": 10,
        "height": 11,
        "scaleByDistance": {
            "nearFarScalar": [ 1.0, 2.0, 10000.0, 3.0 ]
        },
        "translucencyByDistance": {
            "nearFarScalar": [ 1.0, 1.0, 10000.0, 0.0 ]
        },
        "pixelOffsetScaleByDistance": {
            "nearFarScalar": [ 1.0, 20.0, 10000.0, 30.0 ]
        }
    }
}
```

## Properties

**show** - [[Boolean]]

Whether or not the billboard is shown.

Default: `true`


**image** - [[Uri]] - **Required**

The URI of the image displayed on the billboard. For broadest client compatibility, the URI should be accessible via Cross-Origin Resource Sharing (CORS). The URI may also be a <a href="https://developer.mozilla.org/en/data_URIs">data URI</a>.


**scale** - [[Double]]

The scale of the billboard. The scale is multiplied with the pixel size of the billboard's `image`. For example, if the scale is 2.0, the billboard will be rendered with twice the number of pixels, in each direction, of the `image`.

Default: `1.0`


**pixelOffset** - [[PixelOffset]]

The offset, in viewport pixels, of the billboard origin from the `position`. A pixel offset is the number of pixels up and to the right to place the billboard, relative to the `position`.

Default: `[0.0, 0.0]`


**eyeOffset** - [[EyeOffset]]

The eye offset of the billboard, which is the offset in eye coordinates at which to place the billboard relative to the `position` property. Eye coordinates are a left-handed coordinate system where the X-axis points toward the viewer's right, the Y-axis points up, and the Z-axis points into the screen.

Default: `[0.0, 0.0, 0.0]`


**horizontalOrigin** - [[HorizontalOrigin]]

The horizontal origin of the billboard, which determines whether the billboard image is left-, center-, or right-aligned with the `position`.

Default: `CENTER`


**verticalOrigin** - [[VerticalOrigin]]

The vertical origin of the billboard, which determines whether the billboard image is bottom-, center-, or top-aligned with the `position`.

Default: `CENTER`


**heightReference** - [[HeightReference]]

The height reference of the billboard, which indicates if the position is relative to terrain or not.

Default: `NONE`


**color** - [[Color]]

The color of the billboard. This color value is multiplied with the values of the billboard's "image" to produce the final color.

Default: `white`


**rotation** - [[Double]]

The rotation of the billboard, in radians, counter-clockwise from the alignedAxis.

Default: `0.0`


**alignedAxis** - [[AlignedAxis]]

The aligned axis is the unit vector, in world coordinates, that the billboard up vector points towards. The default is the zero vector, which means the billboard is aligned to the screen up vector.

Default: `[0.0, 0.0, 0.0]`


**sizeInMeters** - [[Boolean]]

Whether this billboard's size (`width` and `height`) should be measured in meters, otherwise size is measured in pixels.

Default: `false`


**width** - [[Double]]

The width of the billboard, in pixels (or meters, if `sizeInMeters` is true). By default, the native width of the image is used.


**height** - [[Double]]

The height of the billboard, in pixels (or meters, if `sizeInMeters` is true). By default, the native height of the image is used.


**scaleByDistance** - [[NearFarScalar]]

How the billboard's scale should change based on the billboard's distance from the camera. This scalar value will be multiplied by `scale`.


**translucencyByDistance** - [[NearFarScalar]]

How the billboard's translucency should change based on the billboard's distance from the camera. This scalar value should range from 0 to 1.


**pixelOffsetScaleByDistance** - [[NearFarScalar]]

How the billboard's pixel offset should change based on the billboard's distance from the camera. This scalar value will be multiplied by `pixelOffset`.


**imageSubRegion** - [[BoundingRectangle]]

A sub-region of the image which will be used for the billboard, rather than the entire image, measured in pixels from the bottom-left.


**distanceDisplayCondition** - [[DistanceDisplayCondition]]

The display condition specifying the distance from the camera at which this billboard will be displayed.


**disableDepthTestDistance** - [[Double]]

The distance from the camera at which to disable the depth test. This can be used to prevent clipping against terrain, for example. When set to zero, the depth test is always applied. When set to Infinity, the depth test is never applied.

Default: `0.0`


