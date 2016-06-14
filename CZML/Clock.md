This page describes the possible content of a CZML document or stream.  Please read [[CZML Structure]] for an explanation of how a CZML document is put together.

#Clock

Initial settings for a simulated clock when a document is loaded.  The start and stop time are configured using the interval property.

**Interpolatable**: no

##Properties

**currentTime** - [[Time]]

The current time, specified in ISO8601 format.


**multiplier** - number

The multiplier.  When `step` is set to `TICK_DEPENDENT`, this is the number of seconds to advance each tick.  When `step` is set to `SYSTEM_CLOCK_DEPENDENT`, this is multiplied by the elapsed system time between ticks.  This value is ignored in `SYSTEM_CLOCK` mode.  The default value is 1.0.


**range** - [[ClockRange]]

The behavior when the current time reaches its start or end times.  The default value is `LOOP_STOP`.


**step** - [[ClockStep]]

How the current time advances each tick.  The default value is `SYSTEM_CLOCK_MULTIPLIER`.


