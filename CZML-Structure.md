CZML is a subset of [JSON](http://www.json.org), meaning that a valid CZML document is also a valid JSON document.  Specifically, a CZML document contains a single JSON array where each object-literal element in the array is a CZML [[Packet]].  A CZML packet describes the graphical properties for a single object in the scene, such as a single aircraft.

_Note: we use javascript comments in these examples even though comments are not technically allowed in JSON._

```javascript
[
    // packet one
    {
        "id": "GroundControlStation"
        "position": { "cartographicDegrees": [-75.5, 40.0, 0.0] },
        "point": {
            "color": { "rgba": [0, 0, 255, 255] },
        }
    },
    // packet two
    {
        "id": "PredatorUAV",
        // ...
    }
]
```

Each packet has an `id` property identifying the object it is describing.  IDs do not need to be GUIDs, but they do need to uniquely identify a single object within a CZML source and any other CZML sources loaded into the same scope.

If an `id` is not specified, the client will automatically generate a unique one. However, this prevents later packets from referring to this object in order to, for example, add more data to it.

In addition to the `id`, [Packets](Packet) contain zero or more (but usually one or more) properties defining graphical items to draw related to the object.  In the example above, we've specified that the "GroundControlStation" object has a fixed [[Position]] at [WGS 84](http://en.wikipedia.org/wiki/World_Geodetic_System) longitude -75.5 degrees, latitude 40.0 degrees, and height 0.0 meters, and that a blue [[Point]] is drawn at its location.

There are many standard properties defined for CZML, including properties for adding [points](Point), [billboards](Billboard), [models](Model), [lines](Polyline), and other graphics to the scene.  The available properties are described in detail on the [[Packet]] page, and linked pages for sub-properties and sub-types.  On this page, we are primarily concerned with how the data is structured.  For example, we describe how a property can be specified such that it has two different values over two different intervals of time.

## Intervals

In the most general case, the value of a CZML property is a JSON array, where each element in the array is an object literal defining the value of the property for a different interval of time.  The interval described by any given object literal in the array is specified using an [ISO8601 interval](http://en.wikipedia.org/wiki/ISO_8601#Time_intervals) string in the `interval` property.

```javascript
{
    "id": "myObject",
    "someProperty": [
        {
            "interval": "2012-04-30T12:00:00Z/13:00:00Z",
            "number": 5
        },
        {
            "interval": "2012-04-30T13:00:00Z/14:00:00Z",
            "number": 6
        },
    ]
}
```

Here we define the `someProperty` property over two intervals, the first from noon to 1:00 PM UTC where the value of the property is 5, and the other from 1:00 PM to 2:00 PM UTC where the value of the property is 6.  The value will change instantly when crossing the boundary between two intervals.  We use `number` to indicate the value because this is a number-type property.  Some properties, notably properties that represent position, allow the value to be specified in multiple formats, such as a Cartesian X,Y,Z position or a Cartographic longitude, latitude, height position.  The page for each type lists the types of data supported for each property, and the value names to use with each.

The `interval` property is optional.  If it is not specified, the interval is assumed to span all time.  It doesn't make much sense to specify multiple infinite intervals, or intervals that overlap in general, but if you do, the one later in the CZML file or stream takes precedence.

In the common case that the property has a value over just one interval, the interval list array can be omitted entirely.

```javascript
{
    "id": "myObject",
    "someProperty": {
        "interval": "2012-04-30T12:00:00Z/14:00:00Z",
        "number": 5
    }
}
```

Just as before, the `interval` property can be omitted if it spans all time.  For properties with simple values, like the number property shown above, and with a single value for all time, the value can be given even more compactly:

```javascript
{
    "id": "myObject",
    "someProperty": 5
}
```

This abbreviated notation is valid for any property whose value can be represented with one of the simple JSON data types: string, number, or boolean.

## Composite Values

More complicated composite values, such as a Cartesian position or a color, are represented using JSON arrays.  For a Cartesian position, the array has three elements, corresponding to the X, Y, and Z components of the position, respectively.

```javascript
{
    "id": "myObject",
    "someComplexProperty": {
        "cartesian": [1.0, 2.0, 3.0]
    }
}
```

Composite values must always be specified within an interval, even if that interval is infinite as shown here.  If the value, `[1.0, 2.0, 3.0]`, were allowed as the value of the `complexProperty` directly, it would be necessary for a client interpreting the CZML to look at the contents of the array to determine whether the array is a list of intervals or a single value.  So, for simplicity, we do not allow this.

## Sampled Property Values

So far, we've discussed how to specify a single value for a property for all time, and how to specify different values for a property over different discrete intervals.  Some properties also allow you to specify time-tagged samples which the client will interpolate over to compute the value of the property at any given time.  Times are specified using [ISO8601](http://en.wikipedia.org/wiki/ISO_8601) strings.

```javascript
{
    // ...
    "someInterpolatableProperty": {
        "cartesian": [
            "2012-04-30T12:00Z", 1.0, 2.0, 3.0,
            "2012-04-30T12:01Z", 4.0, 5.0, 6.0,
            "2012-04-30T12:02Z", 7.0, 8.0, 9.0
        ]
    }
}
```

Here we're specifying that the value is `[1.0, 2.0, 3.0]` at noon, `[4.0, 5.0, 6.0]` one minute later, and `[7.0, 8.0, 9.0]` a minute after that.  If the client's current clock is 30 seconds past noon, the value will be a linear interpolation between `[1.0, 2.0, 3.0]` and `[4.0, 5.0, 6.0]`, or `[2.5, 3.5, 4.5]`.

For succinctness, times can also be specified in seconds since an epoch.  While this is potentially less precise than specifying each time using an ISO8601 string, it is usually more than sufficient when the samples span less than a day or when the offsets are whole numbers of seconds.

```javascript
{
    // ...
    "someInterpolatableProperty": {
        "epoch": "2012-04-30T12:00Z",
        "cartesian": [
            0.0, 1.0, 2.0, 3.0,
            60.0, 4.0, 5.0, 6.0,
            120.0, 7.0, 8.0, 9.0
        ]
    }
}
```

Finally, properties specified using time-tagged samples have some additional, optional sub-properties controlling interpolation.

```javascript
{
    // ...
    "someInterpolatableProperty": {
        "epoch": "2012-04-30T12:00Z",
        "cartesian": [
            0.0, 1.0, 2.0, 3.0,
            60.0, 4.0, 5.0, 6.0,
            120.0, 7.0, 8.0, 9.0
        ],
        "interpolationAlgorithm": "LAGRANGE",
        "interpolationDegree": 5
    },
}
```

The `interpolationAlgorithm` specifies the algorithm to use to interpolate a value at a different time from the provided data.  See the table below for the possible values.  The `interpolationDegree` property specifies the degree of the polynomial to use for interpolation.  If these properties are not specified, linear interpolation is used.  See [[InterpolatableProperty]] for a full list of the properties relating to interpolation.

It is not necessary for the time of every sample to fall within the interval that contains it, but the samples will not be used outside their interval.  This is useful to provide better accuracy with higher-degree interpolation.

## EventSource and Streaming

Putting an entire CZML document in one big JSON array makes it difficult to load the document incrementally.  Today's web browsers allow some access to a stream before it is complete, but parsing and interpreting the incomplete data requires slow and cumbersome string manipulations.  To facilitate high-performance streaming, CZML may also be streamed using modern browsers' [server-sent events](http://dev.w3.org/html5/eventsource/) (`EventSource`) API.  When using this API, each CZML packet is streamed to the client as a separate event:

```javascript
event: czml
data: {
    // packet one
}

event: czml
data: {
    // packet two
}
```

As a result, the browser raises an event when each packet is received, containing the data for just that one packet.  This allows us to incrementally process CZML data with excellent performance.

So far, we've perhaps implied that a single object is represented using a single packet that describes all of the graphics associated with that object.  But this is not necessarily the case.  A single CZML stream or document can contain multiple packets with the same `id`, describing different aspects of the same object.

In fact, in some cases, two packets can even describe the same property of an object.  This is useful when the property is defined over many intervals or when an interval contains many time-tagged samples.  By breaking the complete definition of a property into multiple packets, we can get relevant data into Cesium sooner to minimize the time that the user must wait before Cesium starts rendering the scene.

When a client receives a CZML packet, it walks through each property contained in the packet.  For each property, it walks through each interval over which the property is defined.  For each interval, it determines if the specified interval has already been defined for the property.  If the interval has already been defined, the existing interval is updated; otherwise, a new one is created.

When updating an existing interval, any provided sub-property value replaces the existing value, if any.  The only exception is when both the previous property value and the new property value contain time-tagged samples.  In that case, the samples are added to the list of samples for that interval.

When a new interval overlaps existing intervals, the new interval takes precedence and the existing intervals are truncated or removed entirely.  This is important to keep in mind because later intervals will be tested against the truncated intervals when determining whether the interval is new or an update to an existing one.

The samples in an interval must be ordered by increasing time within a single packet.  Across packets, however, it is not necessary for the samples to be provided in any particular order.  However, care must be taken to ensure reasonable interpolation when streaming non-contiguous samples.

## Availability

In addition to the `id` property, CZML packets have one additional special property: `availability`.

```javascript
{
    "id": "PredatorUAV",
    "availability": "2012-04-30T12:00:00Z/14:00:00Z",
    // ...
}
```

The `availability` property indicates when data for an object is available.  If data for an object is known to be available at the current animation time, but the client does not yet have that data (presumably because it will arrive in a later packet), the client could pause with a message like "Buffering..." while it waits to receive the data.  The property can be a single string specifying a single interval, or an array of strings representing intervals.

A later Cesium packet can update this availability if it changes or is found to be incorrect. For example, an SGP4 propagator may report availability for all time, but then later the propagator throws an exception and the availability needs to be adjusted. If this optional property is not present, the object is assumed to be available for all time. Availability is scoped to a particular CZML stream, so two different streams can list different availability for a single object. Within a single stream, the last availability stated for an object is the one in effect and any availabilities in previous packets are ignored. If an object is available at a time, the client expects the object to have at least one property, and it expects all properties that it needs to be defined at that time. If the object doesn't have any properties, or a needed property is defined but not at the animation time, the client could pause animation and wait for more data.

## Extending CZML

CZML can be extended with custom properties.  To minimize conflicts, we recommend that users prefix their custom properties with some sort of identifier.