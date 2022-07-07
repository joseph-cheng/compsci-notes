Wires do not scale as well as transistors (like in [[dennard-scaling|Dennard scaling]]).

With $R$ as resistance, $L$ as wire length, $W$ as wire width, and $H$ as wire height, We see the following relation:

$$R \propto \frac{L}{W \cdot H}$$

Then, with $C$ as wire capacitance to substrate, we get the following:

$$C \propto W \cdot L$$

Then with a simple model of wire charging time $T$, we get the following:

$$T \propto R \times C \propto \frac{L^2}{H}$$

So if the chip area stays the same (or increases), we see that global interconnects (that must cross a fixed distance across the chip) do not get any faster.

![img](https://en.wikichip.org/w/images/thumb/2/20/intel_14nm_gate_interconnect.png/800px-intel_14nm_gate_interconnect.png)

The image above shows Intel's interconnect for its 14nm [[silicon-fabrication|technology node]]. We see that the wires at the top of the image (which are the global interconnects) have a much greater height than the lower down interconnects (which are local, and connect local components, or even gates, to each other). This relates to our previous derivation of the charge-up time of a wire.

Another result we see from our derivation is that halving the length of a wire will decrease charge-up time by 4x, so we might add repeaters to decrease charge up time.