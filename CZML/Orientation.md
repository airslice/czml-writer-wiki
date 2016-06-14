This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Orientation

Defines an orientation.  An orientation is a rotation that takes a vector expressed in the "body" axes of the object and transforms it to the Earth fixed axes.

**Extends**: [[InterpolatableProperty]]

**Interpolatable**: yes

##Properties

**unitQuaternion** - [[UnitQuaternion]]

The orientation specified as a 4-dimensional unit magnitude quaternion, specified as `[X, Y, Z, W]`.


**reference** - [[Reference]]

The orientation specified as a reference to another property.


