# teletype_ARC_scenes
Some scenes to exemplify use of ARC specific OPs 

see my teletype repository...


I implemented 6 ring modes.
Each ring can be set in a separate mode.
The Mode 0 is a bit special since it covers the Euclidean sequencer.
In this mode the TR outputs are internally connected to a ring.

Modes 1,2,3 are „only“ display/set value modes for any purpose.
You can set or get a ring value by SVAL or VAL. You can use it for any purpose in your scripts.
Display mode 1 is for Notes, mode 2 is for increasing values (means the ring lights will increase with VAL, and mode 3 for decreasing values.

Mode 4 and 5 are to configure the Euclidean pattern sequencer (length and phase).

Mode 0(Euclidean controller mode)
Mode 1(pitch display mode)
Mode 2(max Val display mode 0-64) - e.g. for slew rate, length or others
Mode 3(min Val display mode 0-64) - e.g. for Start of pattern or others
Mode 4(Euclidean Length configuration)
Mode 5(Euclidean Phase configuration)

OPs:

ARC.RST

reset/sync of all ring steps to 0

ARC.SYN x

1 on - all rings are synced [default] ; in EUCL Mode to the slowest (longest) ring
0 off

ARC.LEN x

x - length of pattern [default 16]

ARC.PHA x y

x - Ring (0-4)
y - step / phase offset

ARC.MO y

y - set mode of all rings (0 Euclidean,1 Pitch, 2 Max Val, 3 Min Val)

ARC.MO.N x y

x - Ring (0-4)
y - set mode (0 Euclidean,1 Pitch, 2 Max Val, 3 Min Val)

ARC.VAL x - get current value of ring x

x - Ring (0-4)

ARC.SVAL x y - set value of ring x to y

x - Ring (0-4)
y - value (0-64)
