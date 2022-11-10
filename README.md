# BigSpicy- Generating Test to measure Input Capacitance
Capacitances is an important parameter for any chip that we design. The propagation delays of a circuit depend on the capacitances of each and every standard cell.propagation delay is the amount of time it takes for signals to pass between two Flip-Flops. <br>In order to make a chip work faster, we want the worst case delay to be as minimum as possible without violating the setup and hold time. The setup and hold time are maintained so that the clock is not running faster than the logic allows.
## Setup and Hold Time
<b>Setup Time</b>: Setup time is the amount of time required for the input to a Flip-Flop to be stable before a clock edge.<br><br>
<b>Hold TIme</b>: Hold time is the minimum amount of time required for the input to a Flip-Flop to be stable after a clock edge.<br>
<p align="center">
  <img src="https://www.researchgate.net/profile/Bing_Li133/publication/323349911/figure/fig2/AS:601153570103320@1520337588961/Setup-time-t-su-hold-time-t-h-and-clock-to-q-delay-d-cq-of-a-flipflop.png" width="1000"/><br>
  Fig 3. Timing Diagram
</p>



