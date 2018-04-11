This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# UnitSpherical (value)

A unit spherical value specified as `[Clock, Cone]` angles. The clock angle is measured in the XY plane from the positive X axis toward the positive Y axis. The cone angle is the angle from the positive Z axis toward the negative Z axis. If the array has two elements, the value is constant. If it has three or more elements, they are time-tagged samples arranged as `[Time, Clock, Cone, Time, Clock, Cone, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

