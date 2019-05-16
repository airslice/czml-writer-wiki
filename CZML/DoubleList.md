This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# DoubleList

A list of floating-point numbers.

**Interpolatable**: no

## Properties

**array** - [[DoubleListValue]]

The list of values specified as an array of numbers.


**references** - [[ReferenceListValue]]

The list of values specified as references. Each reference is to a property that defines a single value, which may change with time.


**delete** - boolean

Whether the client should delete existing data for this property. Data will be deleted for the containing interval, or if there is no containing interval, then all data. If true, all other properties in this property will be ignored.


