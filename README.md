# GDT_PCB
PCB for drive circuitry and Gate Drive Transfomer, for driving IGBT half-bridge PCBAs in Tesla Coil application

- To be used with the PCB from the either the "IGBT_half_bridge" or "QCW_half_bridge_PCB" repos, 2 off for full bridge setup, 4 for dual full-bridge.
- A hand wound gate drive transformer is required.
  - I am planning to wind one with RG-174 co-ax (for high coupling), with primary side being the shield, secondary being the centre conductor.
  - A full bridge setup needs 2 windings on each core, and won't use all four winding connections or output connectors.
  - Will supply pictures once I have built the PCB and wound the transformers
- To drive extra half bridges a second PCB can be "slaved" to the first using the expansion connection. An output variant has been created named "SLAVE" to show this
- PDF schematics, 3D info, BoMs etc are located within the "Reference Outputs" directory
- Note that the regulator for the "12V" net is actually a 5V output part - anything in the range of 5V-12V should be OK.

Note: changes planned for next revision:
- Likely to use RS485 for gate drive signal input from RJ45 for increased noise immunity.
- Will add power status LED
- "12V" to be renamed to "5V", and supply also used for RS485 receiver
