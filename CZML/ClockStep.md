This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#ClockStep

Defines how a clock advances each tick.  If `TICK_DEPENDENT`, the current time is advanced by `multiplier` seconds each tick.  If `SYSTEM_CLOCK_MULTIPLIER`, the current time is advanced by the amount of system time since the last tick, multiplied by `multiplier`.  If `SYSTEM_CLOCK`, the clock is always set to the current system time.

**Interpolatable**: no

##Values

* `SYSTEM_CLOCK`

* `SYSTEM_CLOCK_MULTIPLIER`

* `TICK_DEPENDENT`

