This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#ClockStep

Defines how a clock advances each tick.

**Interpolatable**: no

##Values

* `TICK_DEPENDENT` - The current time is advanced by `multiplier` seconds each tick.

* `SYSTEM_CLOCK_MULTIPLIER` - The current time is advanced by the amount of system time since the last tick, multiplied by `multiplier`.

* `SYSTEM_CLOCK` - The clock is always set to the current system time.

