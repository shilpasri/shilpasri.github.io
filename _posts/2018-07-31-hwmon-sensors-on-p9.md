---
layout: post
title: Hwmon sensors in P9
---

Hwmon / Lm-sensors
===================

Hwmon or lm-sensors is the standard Linux interface to read sensors.  To read the hwmon sensors one can either
read the individual sensor sysfs files or run the sensors command like below.

For example in P9, the sensors output is as below:

	# sensors
	ibmpowernv-isa-0000
	Adapter: ISA adapter
	Chip 0 Vdd Remote Sense:  +0.85 V  (lowest =  +0.68 V, highest =  +1.09 V)
	Chip 0 Vdn Remote Sense:  +0.74 V  (lowest =  +0.74 V, highest =  +0.74 V)
	Chip 8 Vdd Remote Sense:  +0.68 V  (lowest =  +0.67 V, highest =  +1.08 V)
	Chip 8 Vdn Remote Sense:  +0.74 V  (lowest =  +0.74 V, highest =  +0.74 V)
	Chip 0 Vdd:               +0.88 V  (lowest =  +0.72 V, highest =  +1.10 V)
	Chip 0 Vdn:               +0.74 V  (lowest =  +0.74 V, highest =  +0.74 V)
	Chip 8 Vdd:               +0.70 V  (lowest =  +0.70 V, highest =  +1.08 V)
	Chip 8 Vdn:               +0.74 V  (lowest =  +0.74 V, highest =  +0.74 V)
	Chip 0 Core 0:            +51.0°C  (lowest = +31.0°C, highest = +57.0°C)
	Chip 0 Core 4:            +52.0°C  (lowest = +31.0°C, highest = +58.0°C)
	Chip 0 Core 8:            +52.0°C  (lowest = +30.0°C, highest = +57.0°C)
	Chip 0 Core 12:           +52.0°C  (lowest = +31.0°C, highest = +58.0°C)
	Chip 0 Core 16:           +51.0°C  (lowest = +31.0°C, highest = +55.0°C)
	Chip 0 Core 20:           +51.0°C  (lowest = +31.0°C, highest = +56.0°C)
	Chip 0 Core 24:           +53.0°C  (lowest = +31.0°C, highest = +58.0°C)
	Chip 0 Core 28:           +51.0°C  (lowest = +31.0°C, highest = +55.0°C)
	Chip 0 Core 32:           +55.0°C  (lowest = +31.0°C, highest = +59.0°C)
	Chip 0 Core 36:           +55.0°C  (lowest = +31.0°C, highest = +59.0°C)
	Chip 0 Core 40:           +56.0°C  (lowest = +31.0°C, highest = +60.0°C)
	Chip 0 Core 44:           +55.0°C  (lowest = +31.0°C, highest = +58.0°C)
	Chip 0 Core 48:           +51.0°C  (lowest = +31.0°C, highest = +57.0°C)
	Chip 0 Core 52:           +54.0°C  (lowest = +31.0°C, highest = +59.0°C)
	Chip 0 Core 56:           +52.0°C  (lowest = +31.0°C, highest = +58.0°C)
	Chip 0 Core 60:           +51.0°C  (lowest = +31.0°C, highest = +57.0°C)
	Chip 0 Core 64:           +52.0°C  (lowest = +27.0°C, highest = +56.0°C)
	Chip 0 Core 68:           +52.0°C  (lowest = +27.0°C, highest = +56.0°C)
	Chip 0 Core 72:           +52.0°C  (lowest = +31.0°C, highest = +56.0°C)
	Chip 0 Core 76:           +51.0°C  (lowest = +31.0°C, highest = +56.0°C)
	Chip 0 Core 80:           +51.0°C  (lowest = +30.0°C, highest = +55.0°C)
	Chip 0 Core 84:           +51.0°C  (lowest = +30.0°C, highest = +55.0°C)
	Chip 8 Core 88:           +44.0°C  (lowest = +29.0°C, highest = +59.0°C)
	Chip 8 Core 92:           +43.0°C  (lowest = +29.0°C, highest = +58.0°C)
	Chip 8 Core 96:           +45.0°C  (lowest = +29.0°C, highest = +59.0°C)
	Chip 8 Core 100:          +43.0°C  (lowest = +29.0°C, highest = +56.0°C)
	Chip 8 Core 104:          +44.0°C  (lowest = +29.0°C, highest = +56.0°C)
	Chip 8 Core 108:          +44.0°C  (lowest = +29.0°C, highest = +58.0°C)
	Chip 8 Core 112:          +43.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 116:          +44.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 120:          +44.0°C  (lowest = +29.0°C, highest = +59.0°C)
	Chip 8 Core 124:          +44.0°C  (lowest = +29.0°C, highest = +59.0°C)
	Chip 8 Core 128:          +44.0°C  (lowest = +29.0°C, highest = +59.0°C)
	Chip 8 Core 132:          +44.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 136:          +44.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 140:          +46.0°C  (lowest = +29.0°C, highest = +60.0°C)
	Chip 8 Core 144:          +46.0°C  (lowest = +29.0°C, highest = +60.0°C)
	Chip 8 Core 148:          +43.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 152:          +43.0°C  (lowest = +29.0°C, highest = +56.0°C)
	Chip 8 Core 156:          +44.0°C  (lowest = +29.0°C, highest = +55.0°C)
	Chip 8 Core 160:          +45.0°C  (lowest = +29.0°C, highest = +58.0°C)
	Chip 8 Core 164:          +44.0°C  (lowest = +29.0°C, highest = +58.0°C)
	Chip 8 Core 168:          +44.0°C  (lowest = +29.0°C, highest = +57.0°C)
	Chip 8 Core 172:          +43.0°C  (lowest = +29.0°C, highest = +55.0°C)
	Chip 0 DIMM 0 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 1 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 2 :           +25.0°C  (lowest = +24.0°C, highest = +27.0°C)
	Chip 0 DIMM 3 :           +27.0°C  (lowest = +26.0°C, highest = +28.0°C)
	Chip 0 DIMM 4 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 5 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 6 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 7 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 8 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 9 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 10 :          +25.0°C  (lowest = +25.0°C, highest = +27.0°C)
	Chip 0 DIMM 11 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 12 :          +27.0°C  (lowest = +26.0°C, highest = +29.0°C)
	Chip 0 DIMM 13 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 14 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 DIMM 15 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 0 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 1 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 2 :           +29.0°C  (lowest = +27.0°C, highest = +31.0°C)
	Chip 8 DIMM 3 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 4 :           +26.0°C  (lowest = +26.0°C, highest = +29.0°C)
	Chip 8 DIMM 5 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 6 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 7 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 8 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 9 :            +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 10 :          +25.0°C  (lowest = +25.0°C, highest = +28.0°C)
	Chip 8 DIMM 11 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 12 :          +25.0°C  (lowest = +25.0°C, highest = +28.0°C)
	Chip 8 DIMM 13 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 14 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 8 DIMM 15 :           +0.0°C  (lowest =  +0.0°C, highest =  +0.0°C)
	Chip 0 Nest:              +48.0°C  (lowest = +31.0°C, highest = +52.0°C)
	Chip 8 Nest:              +41.0°C  (lowest = +29.0°C, highest = +51.0°C)
	Chip 0 VRM VDD:           +47.0°C  (lowest = +34.0°C, highest = +50.0°C)
	Chip 8 VRM VDD:           +39.0°C  (lowest = +33.0°C, highest = +49.0°C)
	Chip 0 :                 157.00 W  (lowest =   0.00 W, highest = 218.00 W)
	Chip 0 Vdd:              113.00 W  (lowest =   6.00 W, highest = 159.00 W)
	Chip 0 Vdn:               12.00 W  (lowest =  11.00 W, highest =  14.00 W)
	Chip 8 :                  99.00 W  (lowest =   0.00 W, highest = 187.00 W)
	Chip 8 Vdd:               62.00 W  (lowest =   6.00 W, highest = 133.00 W)
	Chip 8 Vdn:               12.00 W  (lowest =  11.00 W, highest =  14.00 W)
	System:                  426.00 W  (lowest =   0.00 W, highest = 563.00 W)
	APSS 1 :                 127.00 W  (lowest =   0.00 W, highest = 185.00 W)
	APSS 2 :                  71.00 W  (lowest =   0.00 W, highest = 155.00 W)
	APSS 5 :                  31.00 W  (lowest =   0.00 W, highest =  45.00 W)
	APSS 6 :                  29.00 W  (lowest =   0.00 W, highest =  43.00 W)
	APSS 15 :                426.00 W  (lowest =   0.00 W, highest = 563.00 W)
	Chip 0 :                   7.51 MJ
	Chip 0 Vdd:                2.68 MJ
	Chip 0 Vdn:              307.10 kJ
	Chip 8 :                   5.09 MJ
	Chip 8 Vdd:                1.59 MJ
	Chip 8 Vdn:              305.61 kJ
	System:                   21.29 MJ
	APSS 1 :                   5.98 MJ
	APSS 2 :                   3.63 MJ
	APSS 5 :                   1.55 MJ
	APSS 6 :                   1.48 MJ
	APSS 15 :                 21.29 MJ
	Chip 0 Vdd:              +133.90 A  (lowest =  +8.70 A, highest = +192.60 A)
	Chip 0 Vdn:              +17.30 A  (lowest = +15.70 A, highest = +20.10 A)
	Chip 8 Vdd:              +93.00 A  (lowest =  +8.90 A, highest = +159.00 A)
	Chip 8 Vdn:              +17.10 A  (lowest = +15.70 A, highest = +20.00 A)


The hwmon sensors can be found in /sys/class/hwmon/hwmon0/.

	# ls /sys/class/hwmon/hwmon0
	curr1_highest   energy8_label  power10_input          power7_input_lowest   temp16_lowest   temp25_input    temp33_lowest   temp42_input    temp50_lowest   temp5_input     temp68_lowest   temp77_input
	curr1_input     energy9_input  power10_input_highest  power7_label          temp17_highest  temp25_label    temp34_highest  temp42_label    temp51_highest  temp5_label     temp69_highest  temp77_label
	curr1_label     energy9_label  power10_input_lowest   power8_input          temp17_input    temp25_lowest   temp34_input    temp42_lowest   temp51_input    temp5_lowest    temp69_input    temp77_lowest
	curr1_lowest    in1_highest    power10_label          power8_input_highest  temp17_label    temp26_highest  temp34_label    temp43_highest  temp51_label    temp60_highest  temp69_label    temp78_highest

Each sysfs file is of the below format:

	typeX_attribute

- type:  Sensor type

- X: Sensor ID

- attribute: Sensor attribute

The below types of sensors are supported by hwmon:

| Sensor type	| hwmon file name |  Unit		|
|---------------|-----------------|--------------------	|
|  Power	| power	 	  | microWatt   	|
| Temperature	| temp	 	  | millidegree Celsius |
| Current	| curr	 	  | milliampere         |
| Voltage	| in	 	  | millivolt		|
| Energy	| energy	  | microJoule		|


Each hwmon sensor consists of below attributes:

| Attribute		   |  Meaning	    |
|--------------------------|----------------|
| input	 		   | Sensor value   |
| highest or input_highest | Historical max |
| lowest or input_lowest   | Historical min |
| label	 		   | Sensor name    |


For example to read the temperature of a core:

	# cat /sys/class/hwmon/hwmon0/temp1_label
	Chip 0 Core 0

	# cat /sys/class/hwmon/hwmon0/temp1_input
	47000

	# cat /sys/class/hwmon/hwmon0/temp1_highest
	57000

	# cat /sys/class/hwmon/hwmon0/temp1_lowest
	31000

More information on the sysfs files can be found here:
- https://elixir.bootlin.com/linux/v4.18-rc7/source/Documentation/hwmon/sysfs-interface
- https://elixir.bootlin.com/linux/v4.18-rc7/source/Documentation/hwmon/ibmpowernv
