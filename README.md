# teletype_ARC_scenes
Some scenes to exemplify use of ARC specific OPs <br>
<br>
see my teletype repository...<br>
<br>
<br>
6 modes implemented.<br>
Each ring can be set in a separate mode.<br>
The Mode 0 is a bit special since it covers the Euclidean sequencer.<br>
In this mode the TR outputs are internally connected to a ring.<br>
<br>
Modes 1,2,3 are „only“ display/set value modes for any purpose.<br>
You can set or get a ring value by SVAL or VAL. You can use it for any purpose in your scripts.<br>
Display mode 1 is for Notes, mode 2 is for increasing values (means the ring lights will increase with VAL, and mode 3 for decreasing values.
<br>
Mode 4 and 5 are to configure the Euclidean pattern sequencer (length and phase).<br>
<br>
Mode 0(Euclidean controller mode)<br>
Mode 1(pitch display mode)<br>
Mode 2(max Val display mode 0-64) - e.g. for slew rate, length or others<br>
Mode 3(min Val display mode 0-64) - e.g. for Start of pattern or others<br>
Mode 4(Euclidean Length configuration)<br>
Mode 5(Euclidean Phase configuration)<br>
OPs:<br>
ARC.MO x y<br>
<br>
This will change function or display of the rings.<br>
x - Ring (1-4), 0 for all<br>
y - set mode (0 Euclidean,1 Pitch, 2 Max Val, 3 Min Val, 4 config length, 5 config phase)<br>
ARC.VAL x - set/get current value of ring x<br>
<br>
x - Ring (1-4), 0 for all<br>
y - Ring value (0-64)<br>
following OPs are especially for Mode 0 (Euclidean Mode)<br>
ARC.RST<br>
<br>
reset/sync of all ring steps to 0<br>
ARC.SYN x<br>
<br>
1 on - all rings are synced [default] ; in EUCL Mode to the slowest (longest) ring<br>
0 off<br>
ARC.STP x<br>
<br>
x - Next Euclidiean Step of ARC c, 0 for all<br>
<br>
ARC.LEN x y<br>
<br>
x - Ring (1-4) , 0 for all<br>
y - length of pattern [default 16]<br>
ARC.PHA x y<br>
<br>
x - Ring (1-4), 0 for all<br>
y - step / phase offset<br>
ARC.SCR x y - start a script at Euclidean trigger, only in Mode (0)<br>
<br>
x - Ring (1-4), 0 for all<br>
y - Script (1-8)<br>
