This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Spherical (value)

A spherical value `[Clock, Cone, Magnitude]`, with angles in radians and magnitude in meters. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis. If the array has three elements, the value is constant. If it has four or more elements, they are time-tagged samples arranged as `[Time, Clock, Cone, Magnitude, Time, Clock, Cone, Magnitude, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

