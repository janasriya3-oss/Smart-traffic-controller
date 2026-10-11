# Smart-traffic-controller
FPGA-Based Emergency-Aware Traffic Junction Controller Using Verilog HDL on Cyclone II EP2C8T144C8 with Quartus II.

This project implements an FPGA-based emergency-aware traffic junction controller using Verilog HDL. It is designed for the Cyclone II EP2C8T144C8 FPGA board and developed using Quartus II software.

The system automatically controls traffic signals for a four-road junction using a Finite State Machine (FSM) and a timer. When an emergency vehicle is detected through a switch input, the controller gives priority to the selected road after safe Yellow and All-Red transitions.

Key Features

- Automatic traffic signal sequencing for four roads.
- Emergency vehicle priority control.
- Safe transitions using Yellow and All-Red signals.
- Switch-based input control.
- LED-based traffic signal indication.
- FSM-based control logic with timer.
- Verilog HDL implementation.

Hardware Requirements

- Cyclone II EP2C8T144C8 FPGA board
- 5 input switches
- 8 LEDs
- Clock input

Software Requirements

- Quartus II
- Verilog HDL

Input Configuration

- SW[0] – Reset
- SW[1] – Emergency request
- SW[3:2] – Emergency road selection
- SW[4] – Emergency completion

Output Configuration

Two LEDs represent each road's traffic signal:

- "00" – Red
- "01" – Yellow
- "10" – Green

Working Principle

1. The controller cycles through the four roads during normal operation.
2. An emergency request selects the road requiring priority.
3. The active road changes to Yellow, followed by an All-Red clearance interval.
4. The selected emergency road receives a Green signal while the other roads remain Red.
5. After the emergency is cleared, the controller returns to normal operation.

Applications

- Smart traffic junctions
- Emergency vehicle priority systems
- FPGA-based traffic control prototypes
- Digital system design and embedded hardware education

Tools and Technologies

Verilog HDL | FPGA | Cyclone II | Quartus II | Finite State Machine (FSM)

Expected Outcome

A low-cost FPGA-based traffic controller that automates four-road signal sequencing and provides emergency road priority with safe signal transitions.
