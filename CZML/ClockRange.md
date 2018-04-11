This page describes the possible content of a CZML document or stream. Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

# ClockRange

The behavior of a clock when its current time reaches its start or end time.

**Interpolatable**: no

## Values

* `UNBOUNDED` - The clock will continue advancing in the current direction.

* `CLAMPED` - The clock will stop.

* `LOOP_STOP` - When the end time is reached while advancing forward, the clock will jump to the start time, and when the start time is reached while advancing backward, the clock will stop.

