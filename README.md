# PLL_OSU_180
The main purpose of this workshop is to design an On-Chip Clock Multiplier (PLL) and implement the layout using open-source EDA tools such as ngspice and Magic on OSU180nm PDK.

## Section 1 - Introduction and Basics of PLL

### - Intellectual Property

IP's, also known as Macros, are pre-made logic units that can be used repeatedly and are supplied by different vendors. The IP's are manufactured in such a way that they have the most optimum and highest specifications that meet the market requirements. Hence, IP's can help reduce the time to market for chip manufacturers like Samsung or Intel.

### - On-Chip Clock Multiplier (PLL)

#### What is it?

An on-chip Clock Multiplier is an IP, that is used to increase (multiply) the frequency of a clock signal coming from a low frequency source (quartz crystal oscillator). 

<p align="center">
  <img width="600" height="250" src="https://i.imgur.com/j4kFVrW.jpg"
</p>
  <p align="center">
    Figure: Clock Multiplier Circuit Diagram
</p>

#### Why is it used?

There are mainly two types of processors: (i) Synchronous (clock dependent) (ii) Asynchronous (clock independent)

Synchronous processors require clock signals to ensure data signals flows uniformly throughout the chip. Signal flow rate depends on the frequency of the clock signal and by increasing the frequency, we can achieve a higher speed with which the processor can process data/information.

#### How can it be implemented?

An On-chip clock multiplier is also known as a Phase Locked Loop (PLL), a feedback control system that is used to increase the frequency of a reference clock signal. The diagram below outlines the block diagram of a typical PLL:

<p align="center">
  <img width="600" height="200" src="https://i.imgur.com/JAmWoEK.jpg"
</p>
  <p align="center">
    Figure: Typical Block diagram of a Phase Locked Loop (PLL)
</p>

### - IP Design Flow

1. Design Specifications - The specificiations with which the IP should be built. For example, Target frequency (input/output frequencies), Jitter Range, Area Constraints, Duty Cycle etc.
  
2. Literature Review -  Book names: (i) Design of Analog CMOS Integrated Circuits by Behzad Razavi (ii) Design of CMOS Phase-Locked Loops (From Circuit Level to Architecture Level) by Behzad Razavi
  
3. Architectural Design - Design the architecture of the IP (PLL) according to the design specifications. A Multiplexer is used to switch between VCO Mode and PLL Mode.

<p align="center">
  <img width="700" height="300" src="https://i.imgur.com/NSE9cHK.jpg"
</p>
  <p align="center">
    Figure: Architectural diagram of a Phase Locked Loop (PLL)
</p>
  
### - EDA Tools Used (along with OSU180 Library files)

1. Ngspice
2. Magic
  
### - Postlayout Simulation (using Magic)

#### - Inverter Layout Design

<p align="center">
  <img width="400" height="600" src="https://i.ibb.co/D5zTZn2/Inverter-Layout.jpg"
</p>
  <p align="center">
    Figure: Layout Design of an Inverter using Magic
</p>

The above diaagram is the layout representation of an inverter using different metal layers, p/n substrate, n well and contacts.


<p align="center">
  <img width="600" height="200" src="https://i.ibb.co/pJyT12X/Commands-on-Magic.jpg"
</p>
  <p align="center">
    Figure: Commands used to extract the spice netlist from Magic Interface
</p>

<p align="center">
  <img width="600" height="400" src="https://i.ibb.co/4RtqJVd/Inverter-Netlist.jpg"
</p>
  <p align="center">
    Figure: Extracted Netlist from Magic
</p>

By using commands to extract the netlist of the inverter from Magic interface, we are able to get the netlist in our directory and prepare it for simulation in Ngspice.

#### - Phase Frequency Detector Layout Design


<p align="center">
  <img width="400" height="600" src="https://i.ibb.co/nCBdvW1/PFD-Layout.jpg"
</p>
  <p align="center">
    Figure: Layout Design of a PFD using Magic
</p>

The above diaagram is the layout representation of a PFD using different metal layers, p/n substrate, n well and contacts.


<p align="center">
  <img width="600" height="200" src="https://i.ibb.co/ss4WSmD/PFD-Netlist.jpg"
</p>
  <p align="center">
    Figure: Extracted Netlist from Magic
</p>

<p align="center">
  <img width="600" height="400" src="https://i.ibb.co/C1hR1Jr/PFD-Modified-Netlist.jpg"
</p>
  <p align="center">
    Figure: Modified Netlist from Magic for simulation
</p>

<p align="center">
  <img width="600" height="400" src="https://i.ibb.co/Wx7sdHc/PFD-Simulation.jpg"
</p>
  <p align="center">
    Figure: Simulation Waveform for PFD
</p>

By using commands to extract the netlist of the PFD from Magic interface, we are able to get the netlist in our directory and then simulate it in Ngspice.

#### - Voltage Controlled Oscillator Layout Design


