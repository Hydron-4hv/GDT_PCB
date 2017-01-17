# GDT_PCB
PCB for drive circuitry and Gate Drive Transfomer, for driving IGBT half-bridge PCBAs in Tesla Coil application

# WARNING:
The creepage/clearance distances on this PCB between the bridge voltages (i.e. those present of the output of the GDT) and the low voltage circuitry is not large (1mm), and thus nothing connected to this PCB (including the driver controller connected via the RJ45 connectors) should be touched while mains voltage is applied. Unless an isolation tranformer is used to supply the bridge DC bus voltage, everything except mains protective earth should be treated as live.

Notes:
- To be used with the PCB from the either the "IGBT_half_bridge" or "QCW_half_bridge_PCB" repos, 2 off for full bridge setup, 4 for dual full-bridge.
- A hand wound gate drive transformer is required.
  - I am planning to wind one with RG-174 co-ax (for high coupling), with primary side being the shield, secondary being the centre conductor.
  - A full bridge setup needs 2 windings on each core, and won't use all four winding connections or output connectors.
  - Will supply pictures once I have built the PCB and wound the transformers
- To drive extra half bridges a second PCB can be "slaved" to the first using the expansion connection. An output variant has been created named "SLAVE" to show this
- PDF schematics, 3D info, BoMs etc are located within the "Reference Outputs" directory
- Note that the regulator for the "12V" net is actually a 5V output part - anything in the range of 5V-12V should work OK.
- The 24V input can be lowered if the desired gate drive voltage to the IGBTs is less than this.
- The 3x 1000uF 25V capacitors are unnecessarily large for low pulse length applications (e.g. standard non-QCW DRSSTC). These should be replaced by smaller, 35V rated parts if the board is not used in a CW or QCW application.

Note: changes planned for next revision:
- Improve creepage distance as possible. Isolation slots.
- Use RS485 for gate drive signal input from RJ45 for increased noise immunity. (High priority)
- Add power status LED
- "12V" to be renamed to "5V", and supply also used for RS485 receiver
- Use switchmode DC/DC on the PCB rather than in a module
- Capacitor voltage specifications in "Gate Driver" sub section to be increased to 35/50V from 25V. Parts are available in the same package with increased rating.
