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
  <img width="600" height="250" src="https://i.imgur.com/JAmWoEK.jpg"
</p>
  <p align="center">
    Figure: Typical Block diagram of a Phase Locked Loop (PLL)
</p>

### - IP Design Flow

1. Design Specifications - Target frequency (input/output freqs), Jitter, Area Constraints, Duty Cycle etc.
  
2. Literature Review -  Book names
  
3. Architectural Design - VCO Mode and PLL Mode using MUX
  
### - Theory and Fundamental Concepts
  
