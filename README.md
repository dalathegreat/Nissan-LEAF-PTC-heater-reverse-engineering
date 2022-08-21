# Nissan LEAF PTC heater reverse engineering
Tips and tricks on repairing the fragile ZE0 LEAF PTC heater.

## Software
The software on the units changed over the years. Presumably, newer software can be flashed onto the units. This is done with an Atmel compatible flasher (for instance "AVRisp mkII"), and selecting "Atmel MEGA644P" as target CPU. There is an header above the CPU used for flashing. Atmel Studio 7 can be used to either flash or download the current software (help wanted to collect all versions!) 

When repairing a unit, consider updating the software at the same time. See the Software folder for .hex files.

## Part Numbers decoded
- 27143-7269RET - 5.0kW HW B04 SW 2.5 
- 27143-7360RET - 4.0kW HW B04 SW 2.5
- 27143-2796RET - 4.0kW HW B04 SW 2.3
- 27143-2482RET - 5.0kW HW B04 SW 2.3

More I missed? Please let me know!

## Hardware
The hardware is quite unreliable by todays standards.