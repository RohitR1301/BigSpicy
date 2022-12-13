 # BigSpicy

## Flowchart
![image](https://user-images.githubusercontent.com/110079689/200117467-c5c6d165-5011-4002-9b82-d756f3bbd48d.png)

## XDM- File Conversion to Xyce format
Primitives and spice files are needed by BigSpicy but they are not processed in their raw format. The files that are fed to BigSpicy should be in Xyce format as minimal internal processing is required for them. 
#### steps to install XDM on debian Linux 
#### Steps to convert file into Xyce format

## Xyce
### 1) Merge SPEF, Verilog and Spice files into circuit protobuf</n>
After obtaining all the required files that is, 7nm Primitives and Spice files in Xyce format, netlist and spice files. We need to merge them as in order to generate a spice deck the order of ports for each instantiated module are also required which leads to dependency on PDK. We then convert the merged files into protobuf with the help of protoc. 

#### steps to install Xyce on debian Linux 
#### Steps to install protoc
#### Steps to merge file to obtain circuit protobuf
## 2) Generating Module Spice Model and Transistor level Spice
The protobuf file that we have generated in the previous step and PDK spice file are then used to make a whole module spice model.</n>
We then pass the ```--flatten_spice``` argument to convert the whole module spice model into transistor level spice.
## 3) Generating test to measure input capacitance
We take the protobuf file, PDK primitives file and the spice file of our module to generate the test manifest and circuit analysis protobuf files. We then run Xyce to perform tests. 

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
<b>Input Files to these steps<br></b>
<b><br>Output File</b><br> 
<b><br>Steps to follow for generating Test to measure input Capacitance</b><br>

## Running Xyce to perform tests

## 4) Linear and transient analysis
we then perform the linear and transient analysis using Xyce with the help of test manifest and circuit analysis protobuf files. 
## 5) Generating wire and whole module tests
We take the protobuf file, primitives, spice, test manifest and circuit analysis file to generate test for whole module. 
  
## 6) perform analysis on wire and whole module tests
We take Final.pb, PDK primitives, test_manifest, test_analysis, PDK spice decks. Input capacitance and delays will be analysed.

 

