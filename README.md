# WSN_RSSI
RSSI localization within a wireless sensor network of Iris Mote

This work is developed in a Ubuntu environment with [TinyOS](http://www.tinyos.net/). Iris Mote is programmed with a mib520 programming board.

The wireless sensor network is constituted by 5 Iris Mote nodes. There are 4 anchor motes set on the 4 corners of a 2m x 2m square, and 1 target mote to locate.


### Run

1. In the AnchorMote folder, use the command below to program four motes as the anchor motes. Clearly lable the mote number by changing mote#.

	`make iris install,$(mote#) mib520,/dev/ttyUSB0`

2. In the TargetMote folder, use the command below to program the target mote.

	`make iris install,$(mote#) mib520,/dev/ttyUSB0`

3. Connect the target mote to a computer, in main folder, run the flowing command to execute the project.

	`java Project -comm serial@/dev/ttyUSB1:iris`