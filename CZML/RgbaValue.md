This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# Rgba (value)

A color specified as an array of color components `[Red, Green, Blue, Alpha]` where each component is in the range 0-255. If the array has four elements, the color is constant. If it has five or more elements, they are time-tagged samples arranged as `[Time, Red, Green, Blue, Alpha, Time, Red, Green, Blue, Alpha, ...]`, where Time is an ISO 8601 date and time string or seconds since epoch.

**Type**: array

