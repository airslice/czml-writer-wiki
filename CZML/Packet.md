This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Packet

Describes the graphical properties of a single object in a scene, such as a single aircraft.

**Interpolatable**: no

##Properties

**id** - string

The ID of the object described by this packet.  IDs do not need to be GUIDs, but they do need to uniquely identify a single object within a CZML source and any other CZML sources loaded into the same scope.  If this property is not specified, the client will automatically generate a unique one.  However, this prevents later packets from referring to this object in order to add more data to it.


**delete** - boolean

Whether the client should delete all existing data for this object, identified by ID. If true, all other properties in this packet will be ignored.


**name** - string

The name of the object.  It does not have to be unique and is intended for user consumption.


**parent** - string

The ID of the parent object, if any.


**description** - [[String]]

An HTML description of the object.


**clock** - [[Clock]]

The clock settings for the entire data set. Only valid on the document object.


**version** - [[String]]

The CZML version being written. Only valid on the document object.


**availability** - [[TimeIntervalCollection]]

The set of time intervals over which data for an object is available. The property can be a single string specifying a single interval, or an array of strings representing intervals.  A later Cesium packet can update this availability if it changes or is found to be incorrect. For example, an SGP4 propagator may initially report availability for all time, but then later the propagator throws an exception and the availability can be adjusted to end at that time. If this optional property is not present, the object is assumed to be available for all time. Availability is scoped to a particular CZML stream, so two different streams can list different availability for a single object. Within a single stream, the last availability stated for an object is the one in effect and any availabilities in previous packets are ignored. If an object is not available at a time, the client will not draw that object.


**position** - [[Position]]

The position of the object in the world. The position has no direct visual representation, but it is used to locate billboards, labels, and other graphical items attached to the object.

**Examples**:

```javascript
{
    "id": "MyObject",
    "position": {
        "cartographicDegrees": [
            -75.0, 40.0, 0.0
        ]
    }
}
```

```javascript
{
    "id": "InternationalSpaceStation",
    "position": {
        "interpolationAlgorithm": "LAGRANGE",
        "interpolationDegree": 5,
        "referenceFrame": "INERTIAL",
        "epoch": "2012-05-02T12:00:00Z",
        "cartesian": [
            0.0, -6668447.2211117, 1201886.45913705, 146789.427467256,
            60.0, -6711432.84684144, 919677.673492462, -214047.552431458,
            90.0, -6721319.92231553, 776899.784034099, -394198.837519575,
            150.0, -6717826.447064, 488820.628328182, -752924.980158179,
            180.0, -6704450.41462847, 343851.784836767, -931084.800346031,
            240.0, -6654518.44949696, 52891.726433174, -1283967.69137678
        ]
    }
}
```


**orientation** - [[Orientation]]

The orientation of the object in the world.  The orientation has no direct visual representation, but it is used to orient models, cones, pyramids, and other graphical items attached to the object.


**viewFrom** - [[Cartesian3]]

A suggested camera location when viewing this object.  The property is specified as a Cartesian position in the East (x), North (y), Up (z) reference frame relative to the object's position.


**billboard** - [[Billboard]]

A billboard, or viewport-aligned image, sometimes called a marker.  The billboard is positioned in the scene by the `position` property.


**point** - [[Point]]

A point, or viewport-aligned circle.  The point is positioned in the scene by the `position` property.


**label** - [[Label]]

A string of text.  The label is positioned in the scene by the `position` property.


**polyline** - [[Polyline]]

A polyline, which is a line in the scene composed of multiple segments.


**path** - [[Path]]

A path, which is a polyline defined by the motion of an object over time.  The possible vertices of the path are specified by the `position` property.


**polygon** - [[Polygon]]

A polygon, which is a closed figure on the surface of the Earth.


**ellipsoid** - [[Ellipsoid]]

An ellipsoid, which is a closed quadric surface that is a three dimensional analogue of an ellipse.  The ellipsoid is positioned and oriented using the `position` and `orientation` properties.


**model** - [[Model]]

A 3D model.  The model is positioned and oriented using the `position` and `orientation` properties.


**ellipse** - [[Ellipse]]

An ellipse, which is a closed curve on the surface of the Earth.  The ellipse is positioned using the `position` property.


**box** - [[Box]]

A box, which is a closed rectangular cuboid.  The box is positioned and oriented using the `position` and `orientation` properties.


**cylinder** - [[Cylinder]]

A cylinder.  The cylinder is positioned and oriented using the `position` and `orientation` properties.


**corridor** - [[Corridor]]

A corridor, which is a shape defined by a centerline and width.


**agi_conicSensor** - [[ConicSensor]]

A conical sensor volume taking into account occlusion of an ellipsoid, i.e., the globe.  The sensor is is positioned and oriented using the `position` and `orientation` properties.


**agi_customPatternSensor** - [[CustomPatternSensor]]

A custom sensor volume taking into account occlusion of an ellipsoid, i.e., the globe.  The sensor is is positioned and oriented using the `position` and `orientation` properties.


**agi_rectangularSensor** - [[RectangularSensor]]

A rectangular pyramid sensor volume taking into account occlusion of an ellipsoid, i.e., the globe.  The sensor is is positioned and oriented using the `position` and `orientation` properties.


**agi_fan** - [[Fan]]

Defines a fan, which starts at a point or apex and extends in a specified list of directions from the apex.  Each pair of directions forms a face of the fan extending to the specified radius.  The fan is positioned and oriented using the `position` and `orientation` properties.


**agi_vector** - [[Vector]]

Defines a graphical vector that originates at the `position` property and extends in the provided direction for the provided length.  The vector is positioned using the `position` property.


