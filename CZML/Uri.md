This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Uri

A URI value.  The URI can optionally vary with time.

**Interpolatable**: no

**Examples**:

```javascript
{
    "uri": [
        {
            "interval": "2013-01-01T00:00:00Z/2013-01-01T01:00:00Z",
            "uri": "image.png"
        },
        {
            "interval": "2013-01-01T01:00:00Z/2013-01-01T02:00:00Z",
            "uri": "image2.png"
        }
    ]
}
```

## Properties

**uri** - [[UriValue]]
The URI value.


**reference** - [[ReferenceValue]]
The URI specified as a reference to another property.


