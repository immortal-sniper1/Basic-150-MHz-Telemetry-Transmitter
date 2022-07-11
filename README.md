# Basic-150-MHz-Telemetry-Transmitter
 Basic 150MHz Telemetry Transmitter based on  https://github.com/fistlabsdev/150-MHz-Telemetry-Transmitter


Ultra Low Power VHF-Transmitter for Wildlife Radio Tagging

This Transmitter is an adaption of http://http://people.ece.cornell.edu/land/PROJECTS/TRANSMIT/.
It has some minor changes and uses only discrete components as winding all coils etc. manually needs a lot of experienece, luck and effort to get the circuit running well and robust, which I hardly had to experience... I got two versions running stable, one manufactured in THT and one in SMD.

This circuit allows to build a low-cost, tiny, light weight and very low power VHF-pulse-transmitter from scratch. It's purpose is to be used in scientific tracking applications for wildlife and livestock. This is the easiest but most effective transmitter circuit which is known to me.

This circuit is operating on 150 MHz and as all radio transmitters also emitting electromagnetic waves at harmonic frequencies, so be sure that you now your local rules for the emitted frequency spectrum! This report is only a theoretical abstract so there is no legal warranty.

This circuit is based on developments in the early 70s on radio telemetry for wildlife and still base for many transmitters nowadays. Check also R. Kenwards book "A manual for wildlife radio tagging" if you're interested in further information and advanced knowledge in radio tagging.

The circuit is in principle a very simple single-stage oscillator based on the third harmonic of a 50MHz crystal (you can also use a different frequency crystal). Its emitting short pulses of a continuous wave signal. The pulse width and pulsing frequency is determined by a simple RC-network. This transmitter can also be used for simple data modulation using ASK (Amplitude Shift Keying) with On-Off-Keying (OOK) by removing the components Rp and Rc and turning on/off the oscillator by applying/removing voltage (with levels Uin/GND) directly to resistor R1 (Node "EN").


Best results were found with the following values:

C1 = 100 nF
L1 = 100 nH (In THT wind copper coil: 4x0.4mm, diameter 3mm)
R1 = 390 kOhm
C2 = 15 pF
L2 = 1 µH (In THT wind copper coil: 12x0.4mm, diameter 3mm)
NPN = MMBT3904 (In THT: 2N3904)
XTAL = 50 MHz
3rd harmonic determines transmitter frequency

Rp = 0-1 MOhm
Cp = 0-5 µF
Combination of Rp and Cp determine the pulse width and Pulsing frequency.

This circuit can be build on a small pcb (see also eagle schematic and layout in ".../eagle/") or directly solder the THT components to each other as a "flying assembly". As antenna you can use just a piece of copper wire with length lambda/4 which is for 150MHz: 2m/4 = 50 cm

The PCB SMD version got an additional matching capacitor Cm with value 2.2pF which was added in series to the antenna.






