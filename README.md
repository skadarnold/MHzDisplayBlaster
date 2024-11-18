# ST-6A Blaster

This is a fork of the MHzDisplayBlaster by Scrap Computing
https://github.com/scrapcomputing/MHzDisplayBlaster

It has been reworked to clone a ST-6A style display board, particularly designed for a Baby AT style case. This case badged as a Gecco was likely the name of the company that built the computer and not the case. This display board is not a perfect match to a ST-6A display, but was the closest I could identify to the style. It will likely need to be modified for your particular case use.

# Assembly Tips
This video shows assembly of the original MHzDisplayBlaster, which is a similar build process.
- Video showing the assembly of rev.0.1 PCB: https://www.youtube.com/watch?v=a4iVehn7APU
 
# Display Configuration
- Each segment of the 7-segment display is configured individually with a jumper
- Each segment corresponds to a pin in the configuration headers
- You can short that pin with one of the neighboring state pins (forming a `T` shape) to set its state, which can be one of the following:
  1. ON when Turbo switch is OFF (jumper to position 1)
  2. ON when Turbo switch is ON (jumper to position 2)
  3. Always ON (jumper to position 3)
  4. Always OFF (no jumper)

<img src='img/configuration.png' width=480>

# Bill of materials

Gerber files are published in the releases: https://github.com/skadarnold/MHzDisplayBlaster/releases

Reference      | Quantity| Value    | Footprint/Comments
---------------|---------|----------|----------
U1             | 1       |(e.g., LTD-6440G) | 18-DIP (0.600", 15.24mm distance between top and bottom row pins) 2-Digit 7-Segment Display Common Cathode 0.56" Red
J1 J2          | 2       |Conn_02x15| Connector Male PinHeader 2x15 P2.54mm Vertical
J4             | 1       |Conn_01x06| Connector Male PinHeader 1x06 P2.54mm Vertical
R1             | 1       | >= 39 Ohm (100 Ohms recommended)| 3.6 x 1.6mm 1/4 Watt resistor.
R2 R3          | 2       | 330 - 1k Ohm | 3.6 x 1.6mm 1/4 Watt resistor.
U2             | 1       | 74LS04 (	SN7404DR ) | SOIC-14
Jumpers        | 5      |          | 2.54mm pitch jumpers