This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Double (value)

A floating-point number. The value may be a single number, or an array with one element, in which case the value is constant. If it is an array with two or more elements, they are time-tagged samples arranged as `[Time, Value, Time, Value, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: number or array

