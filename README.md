# QA403 Impedance Fixture V2

A test fixture for the QuantAsylum QA403 for measuring impedance based on Matt's blog posts:
* https://quantasylum.com/blogs/news/speaker-impedance-measurements
* https://quantasylum.com/blogs/news/measuring-input-impedance

![PCB only](https://github.com/excitonlabs/QA403-Impedance-Fixture-V2/blob/master/Images/jacks.jpg?raw=true)

This is version two of the text fixture and adds
 * optional attenuation before the inputs to the analyser
 * optional current sense resistor if you just want to use the board for connectivity.

The PCB is fairly flexible, there are three footprints for SMD currents sense resistors and a single through-hole footprint. These are in parallel so the expectation is you place one. The PCB also had an additional BNC for the L- input which may be useful for balanced measurements (BTL etc.).

## Using the attenuators

The analyser cannot have input voltages above 40V RMS, for use with high power amplifiers attenuation is needed. Three resistors form a T-pad before each input that can be used to preserve impedance if need. Alternatively, the T-pad can be reduced to a simple voltage divider by using a 0r resistor in the position before the coaxial socket.

### -6 dB attenuation using voltage divider

Place the following components to reduce the voltage the analysers measured by -6dBV:

R5, R7, R9, R12 = 0r

R6, R8, R10, R11, R13, R14, R15, R16 = 3k3

Voltage divider is a better option in general because it introduces less noise due to the lower resistances.

### -10dB attenuation using T-pad

Place the following components to reduce the voltage the analysers measured by -10dBV:

R5, R6, R7, R8, R9, R10, R11, R12 = 52k

R13, R14, R15, R16 = 72k


## Questions

Forum post https://forum.quantasylum.com/t/comments-welcomed-on-test-fixture-pcb-for-impedance-measurements

## How to get this PCB

1. Order PCBs from a fab. house such as https://jlcpcb.com or email me, I have a few spare ones.
2. Order components from the BOM

## BOM

See datasheets in `/Parts` directory.

* Optional 2 x [MKDSN 1,5/ 2-5,08 1729128, terminal block](https://www.phoenixcontact.com/en-us/products/printed-circuit-board-terminal-mkdsn-15-2-508-1729128)
* Optional 2 x [Neutrik NMJ6HCD2, Jack socket](https://www.neutrik.com/en/product/nmj6hcd2)
* 4  x [TE Connectivity 5221123-2, BNC socket](https://www.te.com/usa-en/product-5221123-2.html)
* 1 x current sense resistor of the following types:
  * 2012 (5025)
  * 1206 (3216)
  * 0805 (2012)
  * Through-hole 

## Examples

![PCB with jack sockets](https://github.com/excitonlabs/QA403-Impedance-Fixture-V2/blob/master/Images/jacks.jpg?raw=true)
![PCB with terminals](https://github.com/excitonlabs/QA403-Impedance-Fixture-V2/blob/master/Images/terminals.jpg?raw=true)
![PCB's back](https://github.com/excitonlabs/QA403-Impedance-Fixture-V2/blob/master/Images/back.jpg?raw=true)
