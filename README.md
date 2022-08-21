# Nissan LEAF PTC heater reverse engineering
Tips and tricks on repairing the fragile 2011-2012 ZE0 LEAF PTC heater.

## Software
The software on the units changed over the years. Presumably, newer software can be flashed onto the units. This is done with an Atmel compatible flasher (for instance "AVRisp mkII"), and selecting "Atmel MEGA644P" as target CPU. There is a place for a 6-pin header above the CPU used for flashing. Solder in a header, Atmel Studio 7 can be used to either flash or download the current software (help wanted to collect all versions!) 

When repairing a unit, consider updating the software at the same time. See the Software folder for .hex files.

## Part Numbers decoded
- 27143-0501RET - 5.0kW HW B04 SW 2.5
- 27143-7269RET - 5.0kW HW B04 SW 2.5 
- 27143-7360RET - 4.0kW HW B04 SW 2.5
- 27143-2796RET - 4.0kW HW B04 SW 2.3
- 27143-2482RET - 5.0kW HW B04 SW 2.3

More I missed? Please let me know!

## Fault codes pointing towards failed PTC or HV Fuse
- B2770 HVAC PTC Heater Circuit
- B2772 HVAC PTC Heater Voltage
- B2773 HVAC PTC Heater Circuit 1
- B2774 HVAC PTC Heater Circuit 2
- B2775 HVAC PTC Heater Circuit 3
- B2776 HVAC PTC Heater Circuit 4

## Hardware
The hardware is quite unreliable by todays standards. It has multiple failure points. Usually when it fails, many components break at the same time. Failures could be, but not limited to:

- Failed 30A 400VDC fuse inside DC/DC converter (not inside PTC element!)
- Broken PCB traces
- Loose PTC element tab (solder break)
- Damaged IGBTs (AUIRG4PH50S , part IRG4PH50S works as replacement)
- Probably more

Most people will opt for a replacement unit, you can either go with a brand new ($$$$), or with a known used one. If you need to replace the PTC, start with replacing the PTC, and see if the heater starts to work. If you still get "Heater voltage" error codes, you need to change the fuse inside the DC/DC junction block.

## Useful links
- PTC & fuse replacement, step-by-step pictures: https://www.youtube.com/watch?v=u19YogcC2H8
- PTC replacement: https://www.youtube.com/watch?v=u19YogcC2H8
- https://www.mynissanleaf.com/viewtopic.php?t=28105
- https://ev-olution.yolasite.com/nissan-leaf-ptc-heater-repair.php
- http://www.japtoys.net/forum/viewtopic.php?f=10&t=3613&start=60#p71462