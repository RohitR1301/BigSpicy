# <p style="font-size:80px">BigSpicy- Generating Test to measure Input Capacitance
Capacitances is an important parameter for any chip that we design. The propagation delays of a circuit depend on the capacitances of each and every standard cell.propagation delay is the amount of time it takes for signals to pass between two Flip-Flops. <br>In order to make a chip work faster, we want the worst case delay to be as minimum as possible without violating the setup and hold time. The setup and hold time are maintained so that the clock is not running faster than the logic allows.
## Setup and Hold Time
In digital designs, each and every flip-flop has some restrictions related to the data with respect to the clock in the form of windows in which data can change or not. There is always a region around the clock edge in which input data should not change at the input of the flip-flop. This is because, if the data changes within this window, we cannot guarantee the output.
<br><br><b>Setup Time</b>: Setup time is the amount of time required for the input to a Flip-Flop to be stable before a clock edge.<br><br>
<b>Hold TIme</b>: Hold time is the minimum amount of time required for the input to a Flip-Flop to be stable after a clock edge.<br>
<p align="center">
 <img src="https://user-images.githubusercontent.com/110080106/201023386-a0506ab5-a057-4626-b28b-656e86990351.png"width="600"/><br><b>
 Fig 1. Timing Diagram</b>
</p>
<br>Setup time and hold time are said to be the backbone of timing analysis. Rightly so, for the chip to function properly, setup and hold timing constraints need to be met properly for each and every flip-flop in the design. If even a single flop exists that does not meet setup and hold requirements for timing paths starting from/ending at it, the design will fail and meta-stability will occur.

## Measuring Input Capacitance in BigSpicy
## Running Xyce to perform tests

