Clock frequency simply related to how often the clock oscillates, which dictates how fast data moves around the CPU, and is thus proportional to chip performance (for the same design).

We cannot increase the clock frequency to infinity because this would break correctness. Since signals do not propagate through wires instantly, we have to ensure that the clock frequency is low enough so that data that is expected to propagate in a single cycle is actually able to. The longest path is called the [[critical-path|critical path]].

We are also limited by power consumption. With voltage $V$ and frequency $f$, we get the following (over a limited range of $V$):
$$f \propto V$$

And then with capacitance $C$, chip area $A$, and power consumption $P$, we get the following:
$$P \propto C \cdot V^2 \cdot f \cdot A$$

Therefore, by increasing clock frequency, we drastically increase power consumption, which increases heat dissipation. Too high power consumption can lead to [[thermal-runaway|thermal runaway]].


